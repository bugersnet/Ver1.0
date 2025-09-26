<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bugger's Net - Learn Programming</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
        }
        
        .progress-ring {
            transform: rotate(-90deg);
        }
        
        .progress-ring-circle {
            transition: stroke-dashoffset 0.35s;
            transform-origin: 50% 50%;
        }
        
        .level-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .question-card {
            animation: slideIn 0.3s ease-out;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .correct-answer {
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
        }
        
        .wrong-answer {
            background: linear-gradient(135deg, #ef4444, #dc2626);
            color: white;
        }
        
        .neutral-answer {
            background: #f3f4f6;
            color: #374151;
        }
    </style>
</head>
<body class="bg-gradient-to-br from-blue-50 to-indigo-100 min-h-screen">
    <!-- Header -->
    <header class="bg-white shadow-lg sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4">
                <div class="flex items-center space-x-3">
                    <div class="w-12 h-12 bg-gradient-to-r from-green-400 to-blue-500 rounded-full flex items-center justify-center">
                        <span class="text-white font-bold text-xl">B</span>
                    </div>
                    <div>
                        <h1 class="text-2xl font-bold text-gray-900">Bugger's Net</h1>
                        <p class="text-sm text-gray-600">Learn Programming from Basics to Pro</p>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <div class="text-right">
                        <p class="text-sm text-gray-600">Follow us:</p>
                        <div class="flex space-x-2">
                            <a href="https://www.instagram.com/_nynoah_?igsh=MXd2b3lueHQ3b3R4bg==" target="_blank" rel="noopener noreferrer" class="text-pink-500 hover:text-pink-600 text-sm">@_nynoah_</a>
                            <span class="text-gray-400">|</span>
                            <a href="https://www.instagram.com/bugersnetofficial?igsh=MzJ3YThpNW9tOXBr" target="_blank" rel="noopener noreferrer" class="text-pink-500 hover:text-pink-600 text-sm">@bugersnetofficial</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        <!-- Language Selection Screen -->
        <div id="languageSelection" class="space-y-8">
            <div class="text-center">
                <h2 class="text-4xl font-bold text-gray-900 mb-4">Choose Your Programming Language</h2>
                <p class="text-xl text-gray-600">Start your journey from basics to professional level</p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="language-card bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-all cursor-pointer border-2 border-transparent hover:border-orange-300" onclick="selectLanguage('html')">
                    <div class="w-16 h-16 bg-orange-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <span class="text-2xl">🌐</span>
                    </div>
                    <h3 class="text-xl font-bold text-center text-gray-900 mb-2">HTML</h3>
                    <p class="text-gray-600 text-center text-sm">Web Structure & Markup</p>
                    <div class="mt-4 bg-gray-200 rounded-full h-2">
                        <div class="bg-orange-500 h-2 rounded-full" style="width: 0%"></div>
                    </div>
                    <p class="text-center text-sm text-gray-500 mt-2">0/100 levels</p>
                </div>
                
                <div class="language-card bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-all cursor-pointer border-2 border-transparent hover:border-red-300" onclick="selectLanguage('java')">
                    <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <span class="text-2xl">☕</span>
                    </div>
                    <h3 class="text-xl font-bold text-center text-gray-900 mb-2">Java</h3>
                    <p class="text-gray-600 text-center text-sm">Object-Oriented Programming</p>
                    <div class="mt-4 bg-gray-200 rounded-full h-2">
                        <div class="bg-red-500 h-2 rounded-full" style="width: 0%"></div>
                    </div>
                    <p class="text-center text-sm text-gray-500 mt-2">0/100 levels</p>
                </div>
                
                <div class="language-card bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-all cursor-pointer border-2 border-transparent hover:border-blue-300" onclick="selectLanguage('cpp')">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <span class="text-2xl">⚡</span>
                    </div>
                    <h3 class="text-xl font-bold text-center text-gray-900 mb-2">C++</h3>
                    <p class="text-gray-600 text-center text-sm">System Programming</p>
                    <div class="mt-4 bg-gray-200 rounded-full h-2">
                        <div class="bg-blue-500 h-2 rounded-full" style="width: 0%"></div>
                    </div>
                    <p class="text-center text-sm text-gray-500 mt-2">0/100 levels</p>
                </div>
                
                <div class="language-card bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-all cursor-pointer border-2 border-transparent hover:border-purple-300" onclick="selectLanguage('algorithms')">
                    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <span class="text-2xl">🧠</span>
                    </div>
                    <h3 class="text-xl font-bold text-center text-gray-900 mb-2">Algorithms</h3>
                    <p class="text-gray-600 text-center text-sm">Problem Solving & Logic</p>
                    <div class="mt-4 bg-gray-200 rounded-full h-2">
                        <div class="bg-purple-500 h-2 rounded-full" style="width: 0%"></div>
                    </div>
                    <p class="text-center text-sm text-gray-500 mt-2">0/100 levels</p>
                </div>
            </div>
        </div>

        <!-- Level Selection Screen -->
        <div id="levelSelection" class="hidden space-y-8">
            <div class="flex items-center justify-between">
                <button onclick="showLanguageSelection()" class="flex items-center space-x-2 text-gray-600 hover:text-gray-900">
                    <span>←</span>
                    <span>Back to Languages</span>
                </button>
                <div class="text-center">
                    <h2 id="selectedLanguageTitle" class="text-3xl font-bold text-gray-900"></h2>
                    <p class="text-gray-600">Choose your level</p>
                </div>
                <div></div>
            </div>
            
            <div id="levelsGrid" class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4">
                <!-- Levels will be generated here -->
            </div>
        </div>

        <!-- Quiz Screen -->
        <div id="quizScreen" class="hidden space-y-6">
            <div class="flex items-center justify-between">
                <button onclick="showLevelSelection()" class="flex items-center space-x-2 text-gray-600 hover:text-gray-900">
                    <span>←</span>
                    <span>Back to Levels</span>
                </button>
                <div class="text-center">
                    <h3 id="quizTitle" class="text-2xl font-bold text-gray-900"></h3>
                    <p id="questionCounter" class="text-gray-600"></p>
                </div>
                <div class="text-right">
                    <div class="w-16 h-16">
                        <svg class="progress-ring w-16 h-16">
                            <circle class="text-gray-200" stroke="currentColor" stroke-width="4" fill="transparent" r="28" cx="32" cy="32"/>
                            <circle id="progressCircle" class="progress-ring-circle text-green-500" stroke="currentColor" stroke-width="4" fill="transparent" r="28" cx="32" cy="32" stroke-dasharray="175.929" stroke-dashoffset="175.929"/>
                        </svg>
                    </div>
                </div>
            </div>
            
            <div id="questionCard" class="question-card bg-white rounded-2xl p-8 shadow-lg">
                <h4 id="questionText" class="text-xl font-semibold text-gray-900 mb-6"></h4>
                <div id="answersContainer" class="space-y-3">
                    <!-- Answers will be generated here -->
                </div>
            </div>
            
            <div class="flex justify-between items-center">
                <div id="feedbackMessage" class="text-lg font-medium"></div>
                <button id="nextButton" onclick="nextQuestion()" class="hidden bg-green-500 hover:bg-green-600 text-white px-6 py-3 rounded-xl font-semibold transition-colors">
                    Next Question
                </button>
            </div>
        </div>

        <!-- Exam Screen -->
        <div id="examScreen" class="hidden space-y-6">
            <div class="text-center">
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Level Exam</h3>
                <p class="text-gray-600 mb-6">Answer all questions to complete this level</p>
            </div>
            
            <div id="examQuestions" class="space-y-6">
                <!-- Exam questions will be generated here -->
            </div>
            
            <div class="text-center">
                <button id="submitExamButton" onclick="submitExam()" class="bg-blue-500 hover:bg-blue-600 text-white px-8 py-4 rounded-xl font-semibold text-lg transition-colors">
                    Submit Exam
                </button>
            </div>
        </div>

        <!-- Results Screen -->
        <div id="resultsScreen" class="hidden space-y-8">
            <div class="text-center">
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Exam Results</h3>
                <div id="scoreDisplay" class="text-6xl font-bold mb-4"></div>
                <div id="scoreBreakdown" class="text-xl text-gray-600 mb-6"></div>
            </div>
            
            <div id="examReview" class="space-y-4">
                <!-- Exam review will be shown here -->
            </div>
            
            <div class="text-center space-x-4">
                <button onclick="retakeLevel()" class="bg-orange-500 hover:bg-orange-600 text-white px-6 py-3 rounded-xl font-semibold transition-colors">
                    Retake Level
                </button>
                <button id="nextLevelButton" onclick="nextLevel()" class="bg-green-500 hover:bg-green-600 text-white px-6 py-3 rounded-xl font-semibold transition-colors">
                    Next Level
                </button>
            </div>
        </div>
    </main>

    <script>
        // Global variables
        let currentLanguage = '';
        let currentLevel = 1;
        let currentQuestion = 0;
        let score = 0;
        let questions = [];
        let examAnswers = [];
        let isExamMode = false;

        // Question database for different languages
        const questionDatabase = {
            html: {
                1: [
                    {
                        question: "What does HTML stand for?",
                        options: ["Hyper Text Markup Language", "High Tech Modern Language", "Home Tool Markup Language", "Hyperlink and Text Markup Language"],
                        correct: 0
                    },
                    {
                        question: "Which HTML tag is used for the largest heading?",
                        options: ["<h6>", "<h1>", "<heading>", "<header>"],
                        correct: 1
                    },
                    {
                        question: "What is the correct HTML element for inserting a line break?",
                        options: ["<break>", "<lb>", "<br>", "<newline>"],
                        correct: 2
                    },
                    {
                        question: "Which attribute specifies the URL of the page the link goes to?",
                        options: ["link", "src", "href", "url"],
                        correct: 2
                    },
                    {
                        question: "What is the correct HTML for creating a hyperlink?",
                        options: ["<a url='http://example.com'>Example</a>", "<a href='http://example.com'>Example</a>", "<link>http://example.com</link>", "<hyperlink>http://example.com</hyperlink>"],
                        correct: 1
                    }
                ]
            },
            java: {
                1: [
                    {
                        question: "What is Java?",
                        options: ["A coffee brand", "A programming language", "An island", "A web browser"],
                        correct: 1
                    },
                    {
                        question: "Which company developed Java?",
                        options: ["Microsoft", "Apple", "Sun Microsystems", "Google"],
                        correct: 2
                    },
                    {
                        question: "What is the extension of Java source files?",
                        options: [".java", ".class", ".jar", ".jav"],
                        correct: 0
                    },
                    {
                        question: "Which method is the entry point of a Java program?",
                        options: ["start()", "main()", "run()", "begin()"],
                        correct: 1
                    },
                    {
                        question: "Java is a _____ programming language.",
                        options: ["Procedural", "Functional", "Object-oriented", "Assembly"],
                        correct: 2
                    }
                ]
            },
            cpp: {
                1: [
                    {
                        question: "What does C++ stand for?",
                        options: ["C Plus Plus", "C Advanced", "C Extended", "C Modern"],
                        correct: 0
                    },
                    {
                        question: "Who developed C++?",
                        options: ["Dennis Ritchie", "Bjarne Stroustrup", "James Gosling", "Guido van Rossum"],
                        correct: 1
                    },
                    {
                        question: "What is the extension of C++ source files?",
                        options: [".c", ".cpp", ".cp", ".cplus"],
                        correct: 1
                    },
                    {
                        question: "Which header file is needed for input/output operations?",
                        options: ["<stdio.h>", "<iostream>", "<input.h>", "<output.h>"],
                        correct: 1
                    },
                    {
                        question: "What symbol is used to end statements in C++?",
                        options: [".", ",", ";", ":"],
                        correct: 2
                    }
                ]
            },
            algorithms: {
                1: [
                    {
                        question: "What is an algorithm?",
                        options: ["A programming language", "A step-by-step procedure to solve a problem", "A computer program", "A data structure"],
                        correct: 1
                    },
                    {
                        question: "Which of the following is NOT a characteristic of a good algorithm?",
                        options: ["Clear and unambiguous", "Well-defined inputs and outputs", "Infinite steps", "Feasible"],
                        correct: 2
                    },
                    {
                        question: "What is the time complexity of linear search?",
                        options: ["O(1)", "O(log n)", "O(n)", "O(n²)"],
                        correct: 2
                    },
                    {
                        question: "Which sorting algorithm has the best average case time complexity?",
                        options: ["Bubble Sort", "Selection Sort", "Quick Sort", "Insertion Sort"],
                        correct: 2
                    },
                    {
                        question: "What does 'Big O' notation describe?",
                        options: ["Memory usage", "Time complexity", "Code readability", "Programming difficulty"],
                        correct: 1
                    }
                ]
            }
        };

        // Generate more questions for higher levels
        function generateQuestionsForLevel(language, level) {
            const baseQuestions = questionDatabase[language][1] || [];
            const generatedQuestions = [];
            
            for (let i = 0; i < 20; i++) {
                const baseIndex = i % baseQuestions.length;
                const baseQuestion = baseQuestions[baseIndex];
                
                // Modify questions slightly for different levels
                const modifiedQuestion = {
                    ...baseQuestion,
                    question: `Level ${level}: ${baseQuestion.question}`,
                };
                
                generatedQuestions.push(modifiedQuestion);
            }
            
            return generatedQuestions;
        }

        function selectLanguage(language) {
            currentLanguage = language;
            showLevelSelection();
        }

        function showLanguageSelection() {
            document.getElementById('languageSelection').classList.remove('hidden');
            document.getElementById('levelSelection').classList.add('hidden');
            document.getElementById('quizScreen').classList.add('hidden');
            document.getElementById('examScreen').classList.add('hidden');
            document.getElementById('resultsScreen').classList.add('hidden');
        }

        function showLevelSelection() {
            document.getElementById('languageSelection').classList.add('hidden');
            document.getElementById('levelSelection').classList.remove('hidden');
            document.getElementById('quizScreen').classList.add('hidden');
            document.getElementById('examScreen').classList.add('hidden');
            document.getElementById('resultsScreen').classList.add('hidden');
            
            const languageNames = {
                html: 'HTML',
                java: 'Java',
                cpp: 'C++',
                algorithms: 'Algorithms'
            };
            
            document.getElementById('selectedLanguageTitle').textContent = languageNames[currentLanguage];
            generateLevels();
        }

        function gen
