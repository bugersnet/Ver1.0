<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BungesNet - Learn to Code</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
        }
        
        .typing-animation {
            border-right: 3px solid #10b981;
            animation: blink 1s infinite;
        }
        
        .typing-cursor {
            border-right: 2px solid #10b981;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { border-color: #10b981; }
            51%, 100% { border-color: transparent; }
        }
        
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .slide-in {
            animation: slideIn 0.3s ease-out;
        }
        
        @keyframes slideIn {
            from { transform: translateX(-100%); }
            to { transform: translateX(0); }
        }
        
        .progress-bar {
            transition: width 0.5s ease-in-out;
        }
        
        .language-card:hover {
            transform: translateY(-5px);
            transition: transform 0.3s ease;
        }
    </style>
</head>
<body class="bg-gradient-to-br from-purple-900 via-blue-900 to-indigo-900 min-h-screen text-white">
    <!-- Header -->
    <header class="bg-black bg-opacity-30 backdrop-blur-sm p-4">
        <div class="container mx-auto flex justify-between items-center">
            <div class="flex items-center space-x-4">
                <h1 id="logo" class="text-3xl font-bold text-green-400 typing-animation"></h1>
            </div>
            <div class="flex space-x-4">
                <a href="https://www.instagram.com/_nynoah_?igsh=MXd2b3lueHQ3b3R4bg==" target="_blank" rel="noopener noreferrer" class="bg-pink-600 hover:bg-pink-700 px-4 py-2 rounded-lg transition-colors">
                    Owner's Instagram
                </a>
                <a href="https://www.instagram.com/bugersnetofficial?igsh=MzJ3YThpNW9tOXBr" target="_blank" rel="noopener noreferrer" class="bg-purple-600 hover:bg-purple-700 px-4 py-2 rounded-lg transition-colors">
                    Community Instagram
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="container mx-auto px-4 py-8">
        <!-- Kali Linux Intro Screen -->
        <div id="kaliIntroScreen" class="flex justify-center items-center min-h-screen">
            <div class="bg-black border-2 border-gray-600 rounded-lg shadow-2xl w-full max-w-4xl">
                <!-- Terminal Header -->
                <div class="bg-gray-800 px-4 py-2 rounded-t-lg flex items-center space-x-2">
                    <div class="w-3 h-3 bg-red-500 rounded-full"></div>
                    <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
                    <div class="w-3 h-3 bg-green-500 rounded-full"></div>
                    <span class="text-gray-300 text-sm ml-4">kali@bugersnet:~$</span>
                </div>
                
                <!-- Terminal Content -->
                <div class="p-6 font-mono text-green-400 bg-black rounded-b-lg" style="min-height: 400px;">
                    <div class="mb-4">
                        <span class="text-blue-400">┌──(</span><span class="text-red-400">kali㉿bugersnet</span><span class="text-blue-400">)-[</span><span class="text-white">~</span><span class="text-blue-400">]</span>
                    </div>
                    <div class="mb-2">
                        <span class="text-blue-400">└─</span><span class="text-red-400">$</span> <span id="terminalCommand" class="typing-cursor"></span>
                    </div>
                    <div id="terminalOutput" class="mt-4 space-y-2 hidden">
                        <div class="text-green-400">Initializing BugersNet Learning Platform...</div>
                        <div class="text-yellow-400">Loading programming modules: C++, HTML, Python, Java, JavaScript</div>
                        <div class="text-blue-400">Setting up 100 levels with 20 questions each...</div>
                        <div class="text-purple-400">Configuring test environment...</div>
                        <div class="text-green-400">✓ System ready!</div>
                        <div class="text-white mt-4">Welcome to BugersNet - Your coding education platform</div>
                        <div class="text-gray-400">Press ENTER to continue...</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Welcome Screen -->
        <div id="welcomeScreen" class="text-center fade-in hidden">
            <h2 class="text-5xl font-bold mb-6 bg-gradient-to-r from-green-400 to-blue-500 bg-clip-text text-transparent">
                Welcome to BugersNet
            </h2>
            <p class="text-xl mb-8 text-gray-300">Learn programming languages step by step, just like Duolingo!</p>
            <button onclick="showLanguageSelection()" class="bg-green-500 hover:bg-green-600 text-white font-bold py-4 px-8 rounded-xl text-xl transition-colors transform hover:scale-105">
                Start Learning
            </button>
        </div>

        <!-- Language Selection -->
        <div id="languageSelection" class="hidden fade-in">
            <h2 class="text-4xl font-bold text-center mb-8">Choose Your Programming Language</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-4xl mx-auto">
                <div class="language-card bg-blue-600 hover:bg-blue-700 p-6 rounded-xl cursor-pointer transition-all" onclick="selectLanguage('cpp')">
                    <h3 class="text-2xl font-bold mb-2">C++</h3>
                    <p class="text-blue-200">Master object-oriented programming</p>
                </div>
                <div class="language-card bg-orange-600 hover:bg-orange-700 p-6 rounded-xl cursor-pointer transition-all" onclick="selectLanguage('html')">
                    <h3 class="text-2xl font-bold mb-2">HTML</h3>
                    <p class="text-orange-200">Build web page structures</p>
                </div>
                <div class="language-card bg-yellow-600 hover:bg-yellow-700 p-6 rounded-xl cursor-pointer transition-all" onclick="selectLanguage('python')">
                    <h3 class="text-2xl font-bold mb-2">Python</h3>
                    <p class="text-yellow-200">Learn programming fundamentals</p>
                </div>
                <div class="language-card bg-red-600 hover:bg-red-700 p-6 rounded-xl cursor-pointer transition-all" onclick="selectLanguage('java')">
                    <h3 class="text-2xl font-bold mb-2">Java</h3>
                    <p class="text-red-200">Enterprise application development</p>
                </div>
                <div class="language-card bg-purple-600 hover:bg-purple-700 p-6 rounded-xl cursor-pointer transition-all" onclick="selectLanguage('javascript')">
                    <h3 class="text-2xl font-bold mb-2">JavaScript</h3>
                    <p class="text-purple-200">Interactive web development</p>
                </div>
            </div>
        </div>

        <!-- Level Selection -->
        <div id="levelSelection" class="hidden fade-in">
            <div class="flex justify-between items-center mb-8">
                <button onclick="showLanguageSelection()" class="bg-gray-600 hover:bg-gray-700 px-4 py-2 rounded-lg">← Back</button>
                <h2 id="languageTitle" class="text-3xl font-bold"></h2>
                <div class="text-right">
                    <p class="text-sm text-gray-300">Progress</p>
                    <p id="overallProgress" class="text-lg font-bold">0/100 Levels</p>
                </div>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4 max-w-6xl mx-auto" id="levelGrid">
                <!-- Levels will be generated here -->
            </div>
        </div>

        <!-- Learning Screen -->
        <div id="learningScreen" class="hidden fade-in">
            <div class="max-w-4xl mx-auto">
                <!-- Progress Bar -->
                <div class="mb-6">
                    <div class="flex justify-between items-center mb-2">
                        <button onclick="showLevelSelection()" class="bg-gray-600 hover:bg-gray-700 px-4 py-2 rounded-lg">← Back</button>
                        <span id="questionProgress" class="text-lg font-semibold">Question 1/20</span>
                    </div>
                    <div class="w-full bg-gray-700 rounded-full h-3">
                        <div id="progressBar" class="progress-bar bg-green-500 h-3 rounded-full" style="width: 5%"></div>
                    </div>
                </div>

                <!-- Question Card -->
                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-8 mb-6">
                    <h3 id="questionTitle" class="text-2xl font-bold mb-4"></h3>
                    <p id="questionText" class="text-lg mb-6"></p>
                    <div id="answerOptions" class="space-y-3">
                        <!-- Answer options will be generated here -->
                    </div>
                </div>

                <!-- Navigation -->
                <div class="flex justify-between">
                    <button id="prevBtn" onclick="previousQuestion()" class="bg-gray-600 hover:bg-gray-700 px-6 py-3 rounded-lg disabled:opacity-50" disabled>Previous</button>
                    <button id="nextBtn" onclick="nextQuestion()" class="bg-green-600 hover:bg-green-700 px-6 py-3 rounded-lg disabled:opacity-50" disabled>Next</button>
                </div>
            </div>
        </div>

        <!-- Test Screen -->
        <div id="testScreen" class="hidden fade-in">
            <div class="max-w-4xl mx-auto">
                <div class="text-center mb-8">
                    <h2 class="text-3xl font-bold mb-4">Level Test</h2>
                    <p class="text-lg text-gray-300">Answer these questions to test your knowledge!</p>
                    <div class="mt-4">
                        <span id="testProgress" class="text-lg font-semibold">Question 1/5</span>
                    </div>
                </div>

                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-8 mb-6">
                    <h3 id="testQuestionTitle" class="text-xl font-bold mb-4"></h3>
                    <p id="testQuestionText" class="text-lg mb-6"></p>
                    <div id="testAnswerOptions" class="space-y-3">
                        <!-- Test answer options will be generated here -->
                    </div>
                </div>

                <div class="flex justify-between">
                    <button id="testPrevBtn" onclick="previousTestQuestion()" class="bg-gray-600 hover:bg-gray-700 px-6 py-3 rounded-lg disabled:opacity-50" disabled>Previous</button>
                    <button id="testNextBtn" onclick="nextTestQuestion()" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-lg disabled:opacity-50" disabled>Next</button>
                </div>
            </div>
        </div>

        <!-- Results Screen -->
        <div id="resultsScreen" class="hidden fade-in">
            <div class="max-w-2xl mx-auto text-center">
                <h2 class="text-4xl font-bold mb-6">Test Results</h2>
                <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-xl p-8 mb-6">
                    <div id="scoreDisplay" class="text-6xl font-bold mb-4 text-green-400"></div>
                    <p id="scoreText" class="text-xl mb-6"></p>
                    <div id="detailedResults" class="text-left space-y-2">
                        <!-- Detailed results will be shown here -->
                    </div>
                </div>
                <div class="space-x-4">
                    <button onclick="retakeTest()" class="bg-yellow-600 hover:bg-yellow-700 px-6 py-3 rounded-lg">Retake Test</button>
                    <button onclick="nextLevel()" class="bg-green-600 hover:bg-green-700 px-6 py-3 rounded-lg">Next Level</button>
                    <button onclick="showLevelSelection()" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-lg">Level Selection</button>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Global variables
        let currentLanguage = '';
        let currentLevel = 1;
        let currentQuestion = 0;
        let currentTestQuestion = 0;
        let userAnswers = [];
        let testAnswers = [];
        let userProgress = {};

        // Typing animation for logo
        function typeWriter() {
            const text = "BugersNet";
            const logo = document.getElementById('logo');
            let i = 0;
            
            function type() {
                if (i < text.length) {
                    logo.textContent += text.charAt(i);
                    i++;
                    setTimeout(type, 150);
                }
            }
            type();
        }

        // Terminal typing animation
        function typeTerminalCommand() {
            const command = "sudo kali linux native";
            const terminalCommand = document.getElementById('terminalCommand');
            let i = 0;
            
            function type() {
                if (i < command.length) {
                    terminalCommand.textContent += command.charAt(i);
                    i++;
                    setTimeout(type, 100);
                } else {
                    setTimeout(() => {
                        showTerminalOutput();
                    }, 1000);
                }
            }
            type();
        }

        function showTerminalOutput() {
            document.getElementById('terminalOutput').classList.remove('hidden');
            setTimeout(() => {
                document.addEventListener('keydown', function(event) {
                    if (event.key === 'Enter') {
                        showWelcomeScreen();
                    }
                });
                // Also allow clicking to continue
                document.getElementById('kaliIntroScreen').addEventListener('click', showWelcomeScreen);
            }, 3000);
        }

        function showWelcomeScreen() {
            document.getElementById('kaliIntroScreen').classList.add('hidden');
            document.getElementById('welcomeScreen').classList.remove('hidden');
        }

        // Initialize the app
        window.onload = function() {
            typeWriter();
            loadProgress();
            setTimeout(typeTerminalCommand, 2000);
        };

        // Sample questions database
        const questionsDB = {
            cpp: {
                1: [
                    {
                        title: "C++ Basics - Variables",
                        question: "Which keyword is used to declare a variable in C++?",
                        options: ["var", "int", "declare", "variable"],
                        correct: 1,
                        explanation: "In C++, 'int' is used to declare integer variables."
                    },
                    {
                        title: "C++ Basics - Output",
                        question: "What is used to output text in C++?",
                        options: ["print()", "cout", "echo", "output"],
                        correct: 1,
                        explanation: "'cout' is the standard output stream in C++."
                    },
                    {
                        title: "C++ Basics - Headers",
                        question: "Which header file is needed for input/output operations?",
                        options: ["<stdio.h>", "<iostream>", "<string.h>", "<math.h>"],
                        correct: 1,
                        explanation: "<iostream> provides input/output stream functionality."
                    },
                    {
                        title: "C++ Basics - Main Function",
                        question: "What is the return type of the main function?",
                        options: ["void", "int", "char", "float"],
                        correct: 1,
                        explanation: "The main function typically returns an int value."
                    },
                    {
                        title: "C++ Basics - Comments",
                        question: "How do you write a single-line comment in C++?",
                        options: ["/* comment */", "// comment", "# comment", "<!-- comment -->"],
                        correct: 1,
                        explanation: "// is used for single-line comments in C++."
                    },
                    {
                        title: "C++ Basics - Semicolon",
                        question: "What character ends most statements in C++?",
                        options: [".", ",", ";", ":"],
                        correct: 2,
                        explanation: "Semicolon (;) terminates most statements in C++."
                    },
                    {
                        title: "C++ Basics - Namespace",
                        question: "Which namespace contains cout and cin?",
                        options: ["system", "std", "io", "stream"],
                        correct: 1,
                        explanation: "std namespace contains standard C++ library functions."
                    },
                    {
                        title: "C++ Basics - Input",
                        question: "What is used to get input from user in C++?",
                        options: ["input", "cin", "get", "read"],
                        correct: 1,
                        explanation: "'cin' is used for standard input in C++."
                    },
                    {
                        title: "C++ Basics - Data Types",
                        question: "Which data type stores decimal numbers?",
                        options: ["int", "char", "float", "bool"],
                        correct: 2,
                        explanation: "'float' stores floating-point (decimal) numbers."
                    },
                    {
                        title: "C++ Basics - Boolean",
                        question: "Which data type stores true/false values?",
                        options: ["int", "bool", "char", "string"],
                        correct: 1,
                        explanation: "'bool' stores boolean (true/false) values."
                    },
                    {
                        title: "C++ Basics - String",
                        question: "How do you declare a string variable?",
                        options: ["str name", "string name", "text name", "char name"],
                        correct: 1,
                        explanation: "'string' is used to declare string variables."
                    },
                    {
                        title: "C++ Basics - Constants",
                        question: "Which keyword makes a variable constant?",
                        options: ["final", "const", "static", "readonly"],
                        correct: 1,
                        explanation: "'const' keyword makes variables constant."
                    },
                    {
                        title: "C++ Basics - Operators",
                        question: "What operator is used for assignment?",
                        options: ["==", "=", "!=", "+="],
                        correct: 1,
                        explanation: "= is the assignment operator in C++."
                    },
                    {
                        title: "C++ Basics - Comparison",
     
