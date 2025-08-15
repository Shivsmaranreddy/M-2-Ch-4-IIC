<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quadratic Equations Analysis</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- KaTeX for LaTeX rendering -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css" xintegrity="sha384-n8MVd4RsNIU0KOVEMckCKLSoHcVHrEPsAnTQSAnMLceLaj8NNApM9NdXPHzOXBIe" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js" xintegrity="sha384-XjKyOOlGwcjNTAIQHIpgOno0Hl1YQqzUOEleOLALmuqehneUG+vnGctmUb0ZY0l8" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js" xintegrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Roboto+Mono&display=swap" rel="stylesheet">

    <style>
        /* Custom styles */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8; /* Light blue-gray background */
        }
        .katex {
            font-size: 1.1em;
        }
        .nav-btn {
            transition: all 0.3s ease;
            border-bottom: 4px solid transparent;
        }
        .nav-btn.active {
            border-bottom-color: #3b82f6; /* Blue-500 */
            color: #1e3a8a; /* Blue-800 */
            font-weight: 600;
        }
        .content-section {
            display: none;
        }
        .content-section.active {
            display: block;
        }
        .card {
            background-color: white;
            border-radius: 0.75rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }
        .solution-toggle {
            cursor: pointer;
            user-select: none;
        }
        .solution-content {
            display: none;
            border-left: 3px solid #3b82f6;
            margin-top: 1rem;
            padding-left: 1rem;
        }
        .prose {
            max-width: none;
        }
    </style>
</head>
<body class="antialiased text-gray-800">

    <div class="container mx-auto p-4 md:p-8">
        <!-- Header -->
        <header class="text-center mb-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-800">Quadratic Expressions & Equations</h1>
            <p class="text-lg text-gray-600 mt-2">A Complete Analysis and Study Guide</p>
        </header>

        <!-- Navigation -->
        <nav class="bg-white rounded-lg shadow-md p-2 mb-8 sticky top-2 z-10">
            <ul class="flex flex-wrap justify-center items-center gap-2 md:gap-6">
                <li><button class="nav-btn active py-2 px-4 text-gray-600 hover:text-blue-600" onclick="showSection('questions')">Question Bank</button></li>
                <li><button class="nav-btn py-2 px-4 text-gray-600 hover:text-blue-600" onclick="showSection('solutions')">Solutions</button></li>
                <li><button class="nav-btn py-2 px-4 text-gray-600 hover:text-blue-600" onclick="showSection('formulae')">Formulae</button></li>
                <li><button class="nav-btn py-2 px-4 text-gray-600 hover:text-blue-600" onclick="showSection('patterns')">Problem Patterns</button></li>
                <li><button class="nav-btn py-2 px-4 text-gray-600 hover:text-blue-600" onclick="showSection('prerequisites')">Prerequisites</button></li>
            </ul>
        </nav>

        <!-- Main Content -->
        <main>
            <!-- Section: Question Bank -->
            <section id="questions" class="content-section active">
                <div class="card">
                    <h2 class="text-2xl font-bold mb-4 text-blue-700">Question Bank (1-65)</h2>
                    <div id="questions-container" class="space-y-6">
                        <!-- Questions will be dynamically rendered here by JS -->
                    </div>
                </div>
            </section>

            <!-- Section: Solutions -->
            <section id="solutions" class="content-section">
                 <div class="card">
                    <h2 class="text-2xl font-bold mb-4 text-blue-700">Solutions (1-65)</h2>
                    <div id="solutions-container" class="space-y-6">
                        <!-- Solutions will be dynamically rendered here by JS -->
                    </div>
                </div>
            </section>

            <!-- Section: Formulae -->
            <section id="formulae" class="content-section">
                <div class="card">
                    <h2 class="text-2xl font-bold mb-4 text-blue-700">Key Formulae & Concepts</h2>
                    <div id="formulae-content" class="space-y-6">
                        <!-- Formulae will be dynamically rendered here by JS -->
                    </div>
                </div>
            </section>

            <!-- Section: Problem Patterns -->
            <section id="patterns" class="content-section">
                <div class="card">
                    <h2 class="text-2xl font-bold mb-4 text-blue-700">Problem Patterns & Classification</h2>
                    <div id="patterns-content" class="space-y-6">
                        <!-- Patterns will be dynamically rendered here by JS -->
                    </div>
                </div>
            </section>

            <!-- Section: Prerequisites -->
            <section id="prerequisites" class="content-section">
                <div class="card">
                    <h2 class="text-2xl font-bold mb-4 text-blue-700">Prerequisite Knowledge</h2>
                    <div id="prerequisites-content" class="prose max-w-none">
                        <p class="mb-4">To effectively solve the problems in this module, a solid understanding of the following foundational concepts is essential:</p>
                        <ul class="list-disc list-inside space-y-2">
                            <li><strong>Algebraic Factorization:</strong> Techniques like splitting the middle term, difference of squares ($a^2-b^2$), and sum/difference of cubes.</li>
                            <li><strong>Quadratic Formula:</strong> For an equation $ax^2+bx+c=0$, the roots are given by $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$.</li>
                            <li><strong>Nature of Roots (Discriminant):</strong> Understanding the discriminant, $\Delta = b^2-4ac$, to determine if roots are real, distinct, equal, or complex.</li>
                            <li><strong>Sum and Product of Roots:</strong> For an equation $ax^2+bx+c=0$ with roots $\alpha$ and $\beta$, we have $\alpha+\beta = -b/a$ and $\alpha\beta = c/a$.</li>
                            <li><strong>Forming a Quadratic Equation:</strong> A quadratic equation with roots $\alpha$ and $\beta$ can be written as $x^2 - (\alpha+\beta)x + \alpha\beta = 0$.</li>
                            <li><strong>Complex Numbers:</strong> Basic operations with imaginary numbers, particularly $i = \sqrt{-1}$.</li>
                            <li><strong>Laws of Indices:</strong> Rules for manipulating exponents, such as $x^{m/n} = \sqrt[n]{x^m}$.</li>
                            <li><strong>Solving Radical and Reciprocal Equations:</strong> Techniques for substitution and simplification for non-standard equation forms.</li>
                            <li><strong>Inequalities:</strong> Solving linear and quadratic inequalities and understanding interval notation.</li>
                        </ul>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <script>
        // --- DATABASE ---
        const questionData = [
            {
                id: 1,
                question: "The roots of $x^2 - 3x + 2 = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The given equation is $x^2 - 3x + 2 = 0$.</li><li>We factor the quadratic by finding two numbers that multiply to 2 and add to -3. These are -1 and -2.</li><li>The factored form is $(x - 1)(x - 2) = 0$.</li><li>Setting each factor to zero gives the roots: $x=1$ and $x=2$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Factoring Quadratics'],
                pattern: 'Finding Roots (Factoring)'
            },
            {
                id: 2,
                question: "The roots of $x^2 - 16 = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The equation is $x^2 - 16 = 0$.</li><li>Add 16 to both sides: $x^2 = 16$.</li><li>Take the square root of both sides, including positive and negative solutions: $x = \\pm\\sqrt{16}$.</li><li>The roots are $x = 4$ and $x = -4$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Difference of Squares'],
                pattern: 'Finding Roots (Square Root Property)'
            },
            {
                id: 3,
                question: "The roots of $4x^2 + 9 = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The equation is $4x^2 + 9 = 0$.</li><li>Rearrange to isolate $x^2$: $4x^2 = -9 \\implies x^2 = -\\frac{9}{4}$.</li><li>Take the square root of both sides: $x = \\pm\\sqrt{-\\frac{9}{4}}$.</li><li>Separate the imaginary part: $x = \\pm\\sqrt{-1} \\cdot \\sqrt{\\frac{9}{4}}$.</li><li>Using $i = \\sqrt{-1}$, we get the roots: $x = \\pm i \\frac{3}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Complex Numbers'],
                pattern: 'Finding Complex Roots'
            },
            {
                id: 4,
                question: "The roots of $x^2 - 4x + 13 = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The equation does not factor easily, so we use the quadratic formula: $x = \\frac{-b \\pm \\sqrt{b^2-4ac}}{2a}$.</li><li>Identify the coefficients: $a=1, b=-4, c=13$.</li><li>Substitute into the formula: $x = \\frac{-(-4) \\pm \\sqrt{(-4)^2 - 4(1)(13)}}{2(1)}$.</li><li>Simplify: $x = \\frac{4 \\pm \\sqrt{16 - 52}}{2} = \\frac{4 \\pm \\sqrt{-36}}{2}$.</li><li>Evaluate the imaginary part: $x = \\frac{4 \\pm 6i}{2}$.</li><li>The final roots are $x = 2 \\pm 3i$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Quadratic Formula'],
                pattern: 'Finding Complex Roots'
            },
            {
                id: 5,
                question: "The roots of $x^2 - 8x + 15 = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The equation is $x^2 - 8x + 15 = 0$.</li><li>We factor by finding two numbers that multiply to 15 and add to -8. These are -3 and -5.</li><li>The factored form is $(x - 3)(x - 5) = 0$.</li><li>The roots are $x=3$ and $x=5$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Factoring Quadratics'],
                pattern: 'Finding Roots (Factoring)'
            },
            {
                id: 6,
                question: "The roots of $\\sqrt{3}x^2 + 10x - 8\\sqrt{3} = 0$ are:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The equation is $\\sqrt{3}x^2 + 10x - 8\\sqrt{3} = 0$.</li><li>We factor by splitting the middle term. Find two numbers that multiply to $ac = (\\sqrt{3})(-8\\sqrt{3}) = -24$ and add to $b=10$. The numbers are 12 and -2.</li><li>Rewrite the equation: $\\sqrt{3}x^2 + 12x - 2x - 8\\sqrt{3} = 0$.</li><li>Factor by grouping: $\\sqrt{3}x(x + 4\\sqrt{3}) - 2(x + 4\\sqrt{3}) = 0$.</li><li>Extract the common factor: $(\\sqrt{3}x - 2)(x + 4\\sqrt{3}) = 0$.</li><li>The roots are $x = \\frac{2}{\\sqrt{3}}$ and $x = -4\\sqrt{3}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Factoring Quadratics'],
                pattern: 'Finding Roots (Factoring)'
            },
            {
                id: 7,
                question: "If $a>0$, $\\sqrt{a+\\sqrt{a+\\sqrt{a+...\\infty}}} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the value of the expression be $x$. So, $x = \\sqrt{a+\\sqrt{a+\\sqrt{a+...}}}$.</li><li>Since the expression is infinite, we can substitute x back into itself: $x = \\sqrt{a+x}$.</li><li>Square both sides to remove the radical: $x^2 = a+x$.</li><li>Rearrange into a standard quadratic equation: $x^2 - x - a = 0$.</li><li>Apply the quadratic formula: $x = \\frac{-(-1) \\pm \\sqrt{(-1)^2 - 4(1)(-a)}}{2(1)} = \\frac{1 \\pm \\sqrt{1+4a}}{2}$.</li><li>Since x represents a positive square root, we take the positive solution: $x = \\frac{1 + \\sqrt{1+4a}}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Solving Radical Equations', 'Quadratic Formula'],
                pattern: 'Infinite Radical Expression'
            },
            {
                id: 8,
                question: "If $20^{3-2x^2} = 40\\sqrt{5}$ then $x=$ (assuming a typo in the question, using $x^2$)",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Assuming the question is $20^{3-2x^2} = 40\\sqrt{5}$.</li><li>Express the right side as a power of 20: $40\\sqrt{5} = 2 \\times 20 \\times \\sqrt{5} = 20 \\times 2\\sqrt{5} = 20 \\times \\sqrt{20} = 20^1 \\times 20^{1/2} = 20^{3/2}$.</li><li>Now the equation is $20^{3-2x^2} = 20^{3/2}$.</li><li>Equate the exponents: $3-2x^2 = \\frac{3}{2}$.</li><li>Solve for $x^2$: $6 - 4x^2 = 3 \\implies 4x^2 = 3 \\implies x^2 = \\frac{3}{4}$.</li><li>Take the square root: $x = \\pm\\sqrt{\\frac{3}{4}} = \\pm\\frac{\\sqrt{3}}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: None of the options match this result. There is likely a typo in the question or options.</p>`,
                formulae: ['Laws of Indices'],
                pattern: 'Exponential Equations'
            },
            {
                id: 9,
                question: "If $x+\\sqrt{x} = \\frac{6}{25}$ then $x=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $y = \\sqrt{x}$. Since $\\sqrt{x}$ must be non-negative, the condition is $y \\ge 0$.</li><li>The equation becomes $y^2 + y = \\frac{6}{25}$.</li><li>Rearrange into a standard quadratic: $25y^2 + 25y - 6 = 0$.</li><li>Use the quadratic formula for y: $y = \\frac{-25 \\pm \\sqrt{25^2 - 4(25)(-6)}}{2(25)} = \\frac{-25 \\pm \\sqrt{1225}}{50} = \\frac{-25 \\pm 35}{50}$.</li><li>The two possible values for y are $y = \\frac{10}{50} = \\frac{1}{5}$ and $y = \\frac{-60}{50} = -\\frac{6}{5}$.</li><li>Apply the condition $y \\ge 0$, so we must choose $y = \\frac{1}{5}$.</li><li>Substitute back to find x: $\\sqrt{x} = \\frac{1}{5} \\implies x = (\\frac{1}{5})^2 = \\frac{1}{25}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Substitution Method', 'Quadratic Formula'],
                pattern: 'Radical Equations'
            },
            {
                id: 10,
                question: "The equation $x-\\frac{2}{x-1} = 1-\\frac{2}{x-1}$ has:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The given equation is $x-\\frac{2}{x-1} = 1-\\frac{2}{x-1}$.</li><li>Note the domain restriction: the denominator cannot be zero, so $x-1 \\neq 0 \\implies x \\neq 1$.</li><li>Add $\\frac{2}{x-1}$ to both sides of the equation. The terms cancel out.</li><li>The equation simplifies to $x = 1$.</li><li>This result, $x=1$, contradicts the domain restriction. Therefore, there is no valid solution.</li></ul><p class='mt-4 font-semibold'>Conclusion: The equation has no root. The correct option is (3).</p>`,
                formulae: ['Domain of Rational Functions'],
                pattern: 'Rational Equations'
            },
            {
                id: 11,
                question: "If $\\sqrt{x+1}-\\sqrt{x-1}=1$ then $x=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Isolate one radical term: $\\sqrt{x+1} = 1 + \\sqrt{x-1}$.</li><li>Square both sides: $(\\sqrt{x+1})^2 = (1 + \\sqrt{x-1})^2 \\implies x+1 = 1 + 2\\sqrt{x-1} + (x-1)$.</li><li>Simplify the equation: $x+1 = x + 2\\sqrt{x-1} \\implies 1 = 2\\sqrt{x-1}$.</li><li>Isolate the remaining radical and square again: $(\\frac{1}{2})^2 = (\\sqrt{x-1})^2 \\implies \\frac{1}{4} = x-1$.</li><li>Solve for x: $x = 1 + \\frac{1}{4} = \\frac{5}{4}$.</li><li>Check for extraneous solutions: $\\sqrt{\\frac{5}{4}+1} - \\sqrt{\\frac{5}{4}-1} = \\sqrt{\\frac{9}{4}} - \\sqrt{\\frac{1}{4}} = \\frac{3}{2} - \\frac{1}{2} = 1$. The solution is valid.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Solving Radical Equations'],
                pattern: 'Radical Equations'
            },
            {
                id: 12,
                question: "The solution of $x^{2/3}+x^{1/3}-2=0$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Use substitution. Let $y = x^{1/3}$.</li><li>The equation becomes a quadratic in y: $y^2+y-2=0$.</li><li>Factor the quadratic: $(y+2)(y-1)=0$.</li><li>The solutions for y are $y=-2$ and $y=1$.</li><li>Substitute back to find x:</li><li class="ml-4">Case 1: $x^{1/3} = -2 \\implies x = (-2)^3 = -8$.</li><li class="ml-4">Case 2: $x^{1/3} = 1 \\implies x = 1^3 = 1$.</li><li>The solution set is $\{1, -8\}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Substitution Method', 'Laws of Indices'],
                pattern: 'Equations in Quadratic Form'
            },
            {
                id: 13,
                question: "If $2x^{1/3}+2x^{-1/3}=5$ then $x=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $y = x^{1/3}$. The equation becomes $2y + \\frac{2}{y} = 5$.</li><li>Multiply by y to clear the fraction: $2y^2 + 2 = 5y$.</li><li>Rearrange into a standard quadratic: $2y^2 - 5y + 2 = 0$.</li><li>Factor the quadratic: $(2y-1)(y-2)=0$.</li><li>The solutions for y are $y=1/2$ and $y=2$.</li><li>Substitute back to find x:</li><li class="ml-4">Case 1: $x^{1/3} = 1/2 \\implies x = (1/2)^3 = 1/8$.</li><li class="ml-4">Case 2: $x^{1/3} = 2 \\implies x = 2^3 = 8$.</li><li>The solutions are 8 or 1/8.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Substitution Method', 'Laws of Indices'],
                pattern: 'Reciprocal Equations'
            },
            {
                id: 14,
                question: "The solution set of $(x-1)(x-3)(x-5)(x-7)=9$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Group the terms symmetrically: $[(x-1)(x-7)][(x-3)(x-5)]=9$.</li><li>Expand the groups: $(x^2 - 8x + 7)(x^2 - 8x + 15) = 9$.</li><li>Use substitution. Let $y = x^2 - 8x$. The equation becomes $(y+7)(y+15)=9$.</li><li>Expand and solve for y: $y^2 + 22y + 105 = 9 \\implies y^2 + 22y + 96 = 0$.</li><li>Factor the quadratic in y: $(y+6)(y+16)=0$. The solutions are $y=-6$ and $y=-16$.</li><li>Substitute back to find x:</li><li class="ml-4">Case 1: $x^2 - 8x = -6 \\implies x^2 - 8x + 6 = 0$. Use the quadratic formula: $x = \\frac{8 \\pm \\sqrt{64-24}}{2} = 4 \\pm \\sqrt{10}$.</li><li class="ml-4">Case 2: $x^2 - 8x = -16 \\implies x^2 - 8x + 16 = 0 \\implies (x-4)^2=0 \\implies x=4$ (a repeated root).</li><li>The solution set is $\{4, 4, 4+\\sqrt{10}, 4-\\sqrt{10}\}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Substitution Method'],
                pattern: 'Polynomial Equations'
            },
            {
                id: 15,
                question: "The solution set of $2(x+\\frac{1}{x})^2-7(x+\\frac{1}{x})+5=0 \\; (x\\ne 0)$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $y = x+\\frac{1}{x}$. The equation becomes $2y^2-7y+5=0$.</li><li>Factor the quadratic in y: $(2y-5)(y-1)=0$.</li><li>The solutions for y are $y=5/2$ and $y=1$.</li><li>Substitute back to find x:</li><li class="ml-4">Case 1: $x+\\frac{1}{x} = \\frac{5}{2} \\implies 2x^2-5x+2=0 \\implies (2x-1)(x-2)=0$. Roots are $x=2, x=1/2$.</li><li class="ml-4">Case 2: $x+\\frac{1}{x} = 1 \\implies x^2-x+1=0$. Use the quadratic formula: $x = \\frac{1 \\pm \\sqrt{1-4}}{2} = \\frac{1 \\pm i\\sqrt{3}}{2}$.</li><li>The complete solution set is $\{2, \\frac{1}{2}, \\frac{1 \pm i\\sqrt{3}}{2}\}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Substitution Method', 'Reciprocal Equations'],
                pattern: 'Equations in Quadratic Form'
            },
            {
                id: 16,
                question: "The solution of $(x^2+\\frac{1}{x^2})-5(x+\\frac{1}{x})+6=0$ when $(x\\ne 0)$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $y = x+\\frac{1}{x}$. Then $y^2 = x^2+2+\\frac{1}{x^2}$, so $x^2+\\frac{1}{x^2} = y^2-2$.</li><li>Substitute into the equation: $(y^2-2) - 5y + 6 = 0$.</li><li>Simplify to a quadratic in y: $y^2-5y+4=0$.</li><li>Factor the quadratic: $(y-1)(y-4)=0$. Solutions are $y=1, y=4$.</li><li>Substitute back to find x:</li><li class="ml-4">Case 1: $x+\\frac{1}{x} = 1 \\implies x^2-x+1=0 \\implies x = \\frac{1 \\pm i\\sqrt{3}}{2}$.</li><li class="ml-4">Case 2: $x+\\frac{1}{x} = 4 \\implies x^2-4x+1=0 \\implies x = \\frac{4 \\pm \\sqrt{16-4}}{2} = 2 \\pm \\sqrt{3}$.</li><li>The solution set is $\{2 \\pm \\sqrt{3}, \\frac{1 \pm i\\sqrt{3}}{2}\}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Substitution Method', 'Reciprocal Equations'],
                pattern: 'Equations in Quadratic Form'
            },
            {
                id: 17,
                question: "If $x=\\frac{-3}{2}$ is a root of the quadratic equation $6x^2+bx+3=0$ then the value of b =",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Since $x=-3/2$ is a root, it satisfies the equation.</li><li>Substitute $x=-3/2$ into the equation: $6(-\\frac{3}{2})^2 + b(-\\frac{3}{2}) + 3 = 0$.</li><li>Simplify: $6(\\frac{9}{4}) - \\frac{3b}{2} + 3 = 0 \\implies \\frac{27}{2} - \\frac{3b}{2} + 3 = 0$.</li><li>Multiply the entire equation by 2: $27 - 3b + 6 = 0$.</li><li>Solve for b: $33 - 3b = 0 \\implies 3b = 33 \\implies b=11$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Root of an Equation'],
                pattern: 'Finding Coefficients'
            },
            {
                id: 18,
                question: "If $x=\\frac{1}{2}$ is a root of the quadratic equation $x^2+kx-\\frac{9}{2}=0$ then $k=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Substitute $x=1/2$ into the equation: $(\\frac{1}{2})^2 + k(\\frac{1}{2}) - \\frac{9}{2} = 0$.</li><li>Simplify: $\\frac{1}{4} + \\frac{k}{2} - \\frac{9}{2} = 0$.</li><li>Multiply the entire equation by 4: $1 + 2k - 18 = 0$.</li><li>Solve for k: $2k - 17 = 0 \\implies 2k = 17 \\implies k = \\frac{17}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: None of the options match. The correct value is $k=8.5$. There is likely a typo in the question or options.</p>`,
                formulae: ['Root of an Equation'],
                pattern: 'Finding Coefficients'
            },
            {
                id: 19,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\alpha^2 + \\beta^2 = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Recall the sum and product of roots: $\\alpha + \\beta = -b/a$ and $\\alpha\\beta = c/a$.</li><li>Use the algebraic identity: $\\alpha^2 + \\beta^2 = (\\alpha + \\beta)^2 - 2\\alpha\\beta$.</li><li>Substitute the root properties into the identity: $\\alpha^2 + \\beta^2 = (-\\frac{b}{a})^2 - 2(\\frac{c}{a})$.</li><li>Simplify the expression: $\\frac{b^2}{a^2} - \\frac{2c}{a}$.</li><li>Combine the terms over a common denominator: $\\frac{b^2 - 2ac}{a^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sum and Product of Roots', 'Algebraic Identities'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 20,
                question: "If $\\alpha, \\beta$ are the roots of $3x^2-5x+7=0$ then $\\alpha^3+\\beta^3 = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Identify the sum and product of roots: $\\alpha+\\beta = -(-5)/3 = 5/3$ and $\\alpha\\beta = 7/3$.</li><li>Use the identity $\\alpha^3+\\beta^3 = (\\alpha+\\beta)^3 - 3\\alpha\\beta(\\alpha+\\beta)$.</li><li>Substitute the values: $\\alpha^3+\\beta^3 = (\\frac{5}{3})^3 - 3(\\frac{7}{3})(\\frac{5}{3})$.</li><li>Calculate: $\\frac{125}{27} - \\frac{105}{9}$.</li><li>Find a common denominator: $\\frac{125}{27} - \\frac{315}{27} = -\\frac{190}{27}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Sum and Product of Roots', 'Algebraic Identities'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 21,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\alpha\\beta^2+\\alpha^2\\beta+\\alpha\\beta = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Factor the common term $\\alpha\\beta$ from the expression: $\\alpha\\beta(\\beta+\\alpha+1)$.</li><li>Recall the sum and product of roots: $\\alpha+\\beta = -b/a$ and $\\alpha\\beta = c/a$.</li><li>Substitute these into the factored expression: $(\\frac{c}{a})(-\\frac{b}{a}+1)$.</li><li>Simplify: $\\frac{c}{a}(\\frac{-b+a}{a}) = \\frac{c(a-b)}{a^2} = \\frac{ac-bc}{a^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 22,
                question: "If $\\alpha, \\beta$ are the roots of $x^2+x+1=0$ then $\\frac{\\alpha}{\\beta}+\\frac{\\beta}{\\alpha} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Combine the terms into a single fraction: $\\frac{\\alpha^2+\\beta^2}{\\alpha\\beta}$.</li><li>From the equation, find the sum and product of roots: $\\alpha+\\beta = -1$ and $\\alpha\\beta=1$.</li><li>Find the value of the numerator: $\\alpha^2+\\beta^2 = (\\alpha+\\beta)^2 - 2\\alpha\\beta = (-1)^2 - 2(1) = -1$.</li><li>Substitute the numerator and denominator values: $\\frac{-1}{1} = -1$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 23,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\frac{1}{\\alpha^2}+\\frac{1}{\\beta^2} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Combine the terms: $\\frac{\\beta^2+\\alpha^2}{\\alpha^2\\beta^2} = \\frac{(\\alpha+\\beta)^2-2\\alpha\\beta}{(\\alpha\\beta)^2}$.</li><li>Substitute the sum and product formulas: $\\alpha+\\beta = -b/a$ and $\\alpha\\beta = c/a$.</li><li>The expression becomes $\\frac{(-b/a)^2-2(c/a)}{(c/a)^2} = \\frac{b^2/a^2 - 2c/a}{c^2/a^2}$.</li><li>Simplify the complex fraction: $\\frac{(b^2-2ac)/a^2}{c^2/a^2} = \\frac{b^2-2ac}{c^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 24,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\frac{\\alpha^2}{\\beta}+\\frac{\\beta^2}{\\alpha} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Combine the terms: $\\frac{\\alpha^3+\\beta^3}{\\alpha\\beta}$.</li><li>Use the identity $\\alpha^3+\\beta^3 = (\\alpha+\\beta)((\\alpha+\\beta)^2-3\\alpha\\beta)$.</li><li>The expression is $\\frac{(\\alpha+\\beta)((\\alpha+\\beta)^2-3\\alpha\\beta)}{\\alpha\\beta}$.</li><li>Substitute $\\alpha+\\beta = -b/a$ and $\\alpha\\beta = c/a$: $\\frac{(-b/a)((-b/a)^2-3(c/a))}{c/a}$.</li><li>Simplify: $\\frac{(-b/a)((b^2-3ac)/a^2)}{c/a} = \\frac{-b(b^2-3ac)}{a^3} \\cdot \\frac{a}{c} = \\frac{3abc-b^3}{a^2c}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 25,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\frac{\\alpha^2+\\beta^2}{\\alpha^{-2}+\\beta^{-2}} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Rewrite the denominator: $\\alpha^{-2}+\\beta^{-2} = \\frac{1}{\\alpha^2}+\\frac{1}{\\beta^2} = \\frac{\\alpha^2+\\beta^2}{(\\alpha\\beta)^2}$.</li><li>The full expression is $\\frac{\\alpha^2+\\beta^2}{(\\alpha^2+\\beta^2)/(\\alpha\\beta)^2}$.</li><li>Assuming $\\alpha^2+\\beta^2 \\neq 0$, cancel the term to get $(\\alpha\\beta)^2$.</li><li>Substitute the product of roots: $(\\alpha\\beta)^2 = (c/a)^2 = \\frac{c^2}{a^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Sum and Product of Roots', 'Laws of Indices'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 26,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $\\frac{\\alpha^3+\\beta^3}{\\alpha^{-3}+\\beta^{-3}} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Rewrite the denominator: $\\alpha^{-3}+\\beta^{-3} = \\frac{1}{\\alpha^3}+\\frac{1}{\\beta^3} = \\frac{\\alpha^3+\\beta^3}{(\\alpha\\beta)^3}$.</li><li>The full expression is $\\frac{\\alpha^3+\\beta^3}{(\\alpha^3+\\beta^3)/(\\alpha\\beta)^3}$.</li><li>Assuming $\\alpha^3+\\beta^3 \\neq 0$, cancel the term to get $(\\alpha\\beta)^3$.</li><li>Substitute the product of roots: $(\\alpha\\beta)^3 = (c/a)^3 = \\frac{c^3}{a^3}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Sum and Product of Roots', 'Laws of Indices'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 27,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $(\\frac{\\alpha}{\\beta}-\\frac{\\beta}{\\alpha})^2 = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Combine the term inside the square: $\\frac{\\alpha^2-\\beta^2}{\\alpha\\beta} = \\frac{(\\alpha-\\beta)(\\alpha+\\beta)}{\\alpha\\beta}$.</li><li>The expression becomes $\\frac{(\\alpha-\\beta)^2(\\alpha+\\beta)^2}{(\\alpha\\beta)^2}$.</li><li>Recall the formulas: $(\\alpha+\\beta)^2 = (-b/a)^2 = b^2/a^2$, $(\\alpha\\beta)^2 = (c/a)^2 = c^2/a^2$, and $(\\alpha-\\beta)^2 = (\\alpha+\\beta)^2 - 4\\alpha\\beta = \\frac{b^2-4ac}{a^2}$.</li><li>Substitute these in: $\\frac{(\\frac{b^2-4ac}{a^2})(\\frac{b^2}{a^2})}{(\\frac{c^2}{a^2})} = \\frac{b^2(b^2-4ac)}{a^4} \\cdot \\frac{a^2}{c^2} = \\frac{b^2(b^2-4ac)}{a^2c^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sum and Product of Roots', 'Difference of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 28,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $(\\frac{1}{\\alpha^2}-\\frac{1}{\\beta^2})^2 = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Combine the term inside the square: $\\frac{\\beta^2-\\alpha^2}{\\alpha^2\\beta^2} = \\frac{-(\\alpha-\\beta)(\\alpha+\\beta)}{(\\alpha\\beta)^2}$.</li><li>The expression becomes $\\frac{(\\alpha-\\beta)^2(\\alpha+\\beta)^2}{(\\alpha\\beta)^4}$.</li><li>Substitute the formulas from the previous question: $\\frac{(\\frac{b^2-4ac}{a^2})(\\frac{b^2}{a^2})}{(\\frac{c}{a})^4} = \\frac{b^2(b^2-4ac)}{a^4} \\cdot \\frac{a^4}{c^4} = \\frac{b^2(b^2-4ac)}{c^4}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Sum and Product of Roots', 'Difference of Roots'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 29,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $(a\\alpha+b)^{-2}+(a\\beta+b)^{-2} = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Since $\\alpha$ is a root, $a\\alpha^2+b\\alpha+c=0$. This implies $\\alpha(a\\alpha+b) = -c$, so $a\\alpha+b = -c/\\alpha$.</li><li>Similarly, for the root $\\beta$, we have $a\\beta+b = -c/\\beta$.</li><li>The expression becomes $(-\\frac{c}{\\alpha})^{-2} + (-\\frac{c}{\\beta})^{-2} = (\\frac{\\alpha}{-c})^2 + (\\frac{\\beta}{-c})^2 = \\frac{\\alpha^2+\\beta^2}{c^2}$.</li><li>We know $\\alpha^2+\\beta^2 = \\frac{b^2-2ac}{a^2}$.</li><li>Substitute this in: $\\frac{(b^2-2ac)/a^2}{c^2} = \\frac{b^2-2ac}{a^2c^2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Sum and Product of Roots', 'Root of an Equation'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 30,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$ then $(\\frac{\\alpha}{a\\beta+b})^3-(\\frac{\\beta}{a\\alpha+b})^3 = $",
                solution: `<ul class="list-disc list-inside space-y-2"><li>From the previous question, we have $a\\beta+b = -c/\\beta$ and $a\\alpha+b = -c/\\alpha$.</li><li>Substitute these into the expression: $(\\frac{\\alpha}{-c/\\beta})^3 - (\\frac{\\beta}{-c/\\alpha})^3$.</li><li>Simplify the terms inside the parentheses: $(-\\frac{\\alpha\\beta}{c})^3 - (-\\frac{\\alpha\\beta}{c})^3$.</li><li>The two terms are identical, so their difference is zero.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Root of an Equation'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 31,
                question: "If $\\alpha, \\beta$ are the roots of equation $8x^2-3x+27=0$ then the value of $(\\frac{\\alpha^2}{\\beta})^{1/3}+(\\frac{\\beta^2}{\\alpha})^{1/3}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Rewrite the expression: $\\frac{\\alpha^{2/3}}{\\beta^{1/3}} + \\frac{\\beta^{2/3}}{\\alpha^{1/3}}$.</li><li>Combine over a common denominator $(\\alpha\\beta)^{1/3}$: $\\frac{\\alpha^{2/3}\\alpha^{1/3} + \\beta^{2/3}\\beta^{1/3}}{(\\alpha\\beta)^{1/3}} = \\frac{\\alpha+\\beta}{(\\alpha\\beta)^{1/3}}$.</li><li>From the equation, find the sum and product of roots: $\\alpha+\\beta = -(-3)/8 = 3/8$ and $\\alpha\\beta = 27/8$.</li><li>Substitute these values: $\\frac{3/8}{(27/8)^{1/3}} = \\frac{3/8}{3/2}$.</li><li>Simplify the fraction: $\\frac{3}{8} \\cdot \\frac{2}{3} = \\frac{2}{8} = \\frac{1}{4}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Sum and Product of Roots', 'Laws of Indices'],
                pattern: 'Symmetric Functions of Roots'
            },
            {
                id: 32,
                question: "If the equation $9x^2+kx+1=0$ has equal roots then $k=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>For an equation to have equal roots, its discriminant must be zero: $\\Delta = b^2-4ac = 0$.</li><li>Identify coefficients: $a=9, b=k, c=1$.</li><li>Set up the discriminant equation: $k^2 - 4(9)(1) = 0$.</li><li>Solve for k: $k^2 - 36 = 0 \\implies k^2 = 36 \\implies k = \\pm 6$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Discriminant'],
                pattern: 'Nature of Roots'
            },
            {
                id: 33,
                question: "If the equation $(3m+1)x^2+2(m+1)x+m=0$ has equal roots then $m=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>For equal roots, set the discriminant to zero: $\\Delta = b^2-4ac = 0$.</li><li>Identify coefficients: $a=3m+1, b=2(m+1), c=m$.</li><li>Set up the equation: $(2(m+1))^2 - 4(3m+1)(m) = 0$.</li><li>Expand and simplify: $4(m^2+2m+1) - 4(3m^2+m) = 0$.</li><li>Divide by 4: $(m^2+2m+1) - (3m^2+m) = 0 \\implies -2m^2+m+1=0$.</li><li>Multiply by -1 and factor: $2m^2-m-1=0 \\implies (2m+1)(m-1)=0$.</li><li>The solutions are $m=-1/2$ and $m=1$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Discriminant'],
                pattern: 'Nature of Roots'
            },
            {
                id: 34,
                question: "If the roots of $(c^2-ab)x^2-2(a^2-bc)x+(b^2-ac)=0$ are equal then:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>For equal roots, $\\Delta = B^2-4AC=0$.</li><li>Identify coefficients: $A=c^2-ab, B=-2(a^2-bc), C=b^2-ac$.</li><li>Set up the equation: $(-2(a^2-bc))^2 - 4(c^2-ab)(b^2-ac) = 0$.</li><li>Expand: $4(a^4-2a^2bc+b^2c^2) - 4(b^2c^2-ac^3-ab^3+a^2bc) = 0$.</li><li>Divide by 4 and simplify: $a^4-2a^2bc+b^2c^2 - b^2c^2+ac^3+ab^3-a^2bc = 0$.</li><li>Combine terms: $a^4+ab^3+ac^3-3a^2bc = 0$.</li><li>Factor out 'a': $a(a^3+b^3+c^3-3abc) = 0$.</li><li>This implies either $a=0$ or $a^3+b^3+c^3-3abc=0$, which is equivalent to $a^3+b^3+c^3=3abc$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Discriminant', 'Algebraic Identities'],
                pattern: 'Nature of Roots'
            },
            {
                id: 35,
                question: "The quadratic equation whose roots are $\\frac{1}{3+\\sqrt{2}}$ and $\\frac{1}{3-\\sqrt{2}}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the roots be $\\alpha$ and $\\beta$. Rationalize them first.</li><li>$\\alpha = \\frac{1}{3+\\sqrt{2}} \\times \\frac{3-\\sqrt{2}}{3-\\sqrt{2}} = \\frac{3-\\sqrt{2}}{9-2} = \\frac{3-\\sqrt{2}}{7}$.</li><li>$\\beta = \\frac{1}{3-\\sqrt{2}} \\times \\frac{3+\\sqrt{2}}{3+\\sqrt{2}} = \\frac{3+\\sqrt{2}}{9-2} = \\frac{3+\\sqrt{2}}{7}$.</li><li>Calculate the sum of roots (S): $S = \\alpha+\\beta = \\frac{3-\\sqrt{2}+3+\\sqrt{2}}{7} = \\frac{6}{7}$.</li><li>Calculate the product of roots (P): $P = \\alpha\\beta = (\\frac{3-\\sqrt{2}}{7})(\\frac{3+\\sqrt{2}}{7}) = \\frac{9-2}{49} = \\frac{1}{7}$.</li><li>Form the equation using $x^2-Sx+P=0$: $x^2 - \\frac{6}{7}x + \\frac{1}{7} = 0$.</li><li>Multiply by 7 to clear denominators: $7x^2-6x+1=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Forming a Quadratic Equation', 'Rationalization'],
                pattern: 'Forming Equations from Roots'
            },
            {
                id: 36,
                question: "The quadratic equation whose roots are $3+2i, 3-2i$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The roots are a complex conjugate pair. Let $\\alpha=3+2i$ and $\\beta=3-2i$.</li><li>Calculate the sum of roots (S): $S = (3+2i)+(3-2i)=6$.</li><li>Calculate the product of roots (P): $P = (3+2i)(3-2i) = 3^2-(2i)^2 = 9-4i^2 = 9+4=13$.</li><li>Form the equation using $x^2-Sx+P=0$: $x^2-6x+13=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Forming a Quadratic Equation', 'Complex Numbers'],
                pattern: 'Forming Equations from Roots'
            },
            {
                id: 37,
                question: "If $\\alpha, \\beta$ are the roots of $ax^2+bx+c=0$, and $px^2+qx+r=0$ has roots $\\frac{1-\\alpha}{\\alpha}$ and $\\frac{1-\\beta}{\\beta}$, then $r=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the new root be $y$. We have the transformation $y = \\frac{1-x}{x}$.</li><li>To find the new equation, we express x in terms of y: $yx = 1-x \\implies yx+x=1 \\implies x(y+1)=1 \\implies x = \\frac{1}{y+1}$.</li><li>Substitute this into the original equation: $a(\\frac{1}{y+1})^2 + b(\\frac{1}{y+1}) + c = 0$.</li><li>Multiply by $(y+1)^2$: $a + b(y+1) + c(y+1)^2 = 0$.</li><li>Expand: $a + by+b + c(y^2+2y+1) = 0 \\implies a+by+b+cy^2+2cy+c=0$.</li><li>Group terms: $cy^2 + (b+2c)y + (a+b+c) = 0$.</li><li>Comparing this to $py^2+qy+r=0$, we see that $r$ corresponds to the constant term, $a+b+c$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Transformation of Roots', 'Sum and Product of Roots'],
                pattern: 'Transformation of Equations'
            },
            {
                id: 38,
                question: "If $\\alpha, \\beta$ are the roots of $9x^2+6x+1=0$ then the equation with the roots $\\frac{1}{\\alpha}, \\frac{1}{\\beta}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the new root be $y = 1/x$, which means $x=1/y$.</li><li>Substitute this transformation into the original equation: $9(\\frac{1}{y})^2 + 6(\\frac{1}{y}) + 1 = 0$.</li><li>Simplify: $\\frac{9}{y^2} + \\frac{6}{y} + 1 = 0$.</li><li>Multiply by $y^2$ to clear the denominator: $9 + 6y + y^2 = 0$.</li><li>Rewrite in standard form and replace y with x: $x^2+6x+9=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Transformation of Roots'],
                pattern: 'Transformation of Equations'
            },
            {
                id: 39,
                question: "If $\\alpha, \\beta$ are the roots of $2x^2+x+3=0$ then the equation whose roots are $\\frac{1-\\alpha}{1+\\alpha}$ and $\\frac{1-\\beta}{1+\\beta}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the new root be $y = \\frac{1-x}{1+x}$. Express x in terms of y: $y(1+x) = 1-x \\implies x(y+1) = 1-y \\implies x = \\frac{1-y}{1+y}$.</li><li>Substitute this into the original equation: $2(\\frac{1-y}{1+y})^2 + (\\frac{1-y}{1+y}) + 3 = 0$.</li><li>Multiply by $(1+y)^2$: $2(1-y)^2 + (1-y)(1+y) + 3(1+y)^2 = 0$.</li><li>Expand the terms: $2(1-2y+y^2) + (1-y^2) + 3(1+2y+y^2) = 0$.</li><li>Distribute and combine like terms: $(2-4y+2y^2) + (1-y^2) + (3+6y+3y^2) = 0$. This simplifies to $4y^2+2y+6=0$.</li><li>Divide by 2: $2y^2+y+3=0$. Replace y with x: $2x^2+x+3=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Transformation of Roots'],
                pattern: 'Transformation of Equations'
            },
            {
                id: 40,
                question: "If $\\alpha, \\beta$ are the roots of $x^2+5x-4=0$ then the equation whose roots are $\\frac{\\alpha+2}{3}, \\frac{\\beta+2}{3}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the new root be $y = \\frac{x+2}{3}$. Express x in terms of y: $3y = x+2 \\implies x = 3y-2$.</li><li>Substitute this into the original equation: $(3y-2)^2 + 5(3y-2) - 4 = 0$.</li><li>Expand: $(9y^2-12y+4) + (15y-10) - 4 = 0$.</li><li>Combine like terms: $9y^2 + 3y - 10 = 0$.</li><li>Replace y with x: $9x^2+3x-10=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Transformation of Roots'],
                pattern: 'Transformation of Equations'
            },
            {
                id: 41,
                question: "If $3p^2=5p+2$ and $3q^2=5q+2$ where $p \\ne q$, then the equation whose roots are $3p-2q$ and $3q-2p$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The given conditions show that p and q are the distinct roots of the equation $3x^2-5x-2=0$.</li><li>From this, find the sum and product of roots: $p+q = -(-5)/3 = 5/3$ and $pq = -2/3$.</li><li>Let the new roots be $\\alpha = 3p-2q$ and $\\beta = 3q-2p$.</li><li>Find the new sum S: $S = \\alpha+\\beta = (3p-2q)+(3q-2p) = p+q = 5/3$.</li><li>Find the new product P: $P = \\alpha\\beta = (3p-2q)(3q-2p) = 13pq - 6(p^2+q^2)$.</li><li>First find $p^2+q^2 = (p+q)^2 - 2pq = (5/3)^2 - 2(-2/3) = 25/9 + 4/3 = 37/9$.</li><li>Now find P: $P = 13(-2/3) - 6(37/9) = -26/3 - 74/3 = -100/3$.</li><li>Form the new equation $x^2 - Sx + P = 0$: $x^2 - (5/3)x - 100/3 = 0$.</li><li>Multiply by 3: $3x^2 - 5x - 100 = 0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sum and Product of Roots', 'Forming a Quadratic Equation'],
                pattern: 'Transformation of Equations'
            },
            {
                id: 42,
                question: "If $\\alpha, \\beta$ are roots of $x^2+2ax+b=0$, find the quadratic equation with rational coefficients, one of whose roots is $\\alpha+\\beta+\\sqrt{\\alpha^2+\\beta^2}$.",
                solution: `<ul class="list-disc list-inside space-y-2"><li>From the equation, find sum and product: $\\alpha+\\beta = -2a$ and $\\alpha\\beta=b$.</li><li>Calculate $\\alpha^2+\\beta^2 = (\\alpha+\\beta)^2 - 2\\alpha\\beta = (-2a)^2 - 2b = 4a^2-2b$.</li><li>One root of the new equation is $\\gamma = (\\alpha+\\beta) + \\sqrt{\\alpha^2+\\beta^2} = -2a + \\sqrt{4a^2-2b}$.</li><li>Since coefficients must be rational, the other root must be the conjugate: $\\delta = -2a - \\sqrt{4a^2-2b}$.</li><li>Find the new sum S: $S = \\gamma+\\delta = (-2a+\\sqrt{...}) + (-2a-\\sqrt{...}) = -4a$.</li><li>Find the new product P: $P = \\gamma\\delta = (-2a)^2 - (\\sqrt{4a^2-2b})^2 = 4a^2 - (4a^2-2b) = 2b$.</li><li>Form the new equation $x^2-Sx+P=0$: $x^2 - (-4a)x + 2b = 0 \\implies x^2+4ax+2b=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Sum and Product of Roots', 'Conjugate Roots'],
                pattern: 'Forming Equations from Roots'
            },
            {
                id: 43,
                question: "The quadratic equation for which the sum of the roots is 7 and the sum of the squares of the roots is 25 is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the roots be $\\alpha, \\beta$. Given: $\\alpha+\\beta = 7$ and $\\alpha^2+\\beta^2=25$.</li><li>The required equation is $x^2 - (\\alpha+\\beta)x + \\alpha\\beta = 0$. We need to find $\\alpha\\beta$.</li><li>Use the identity $\\alpha^2+\\beta^2 = (\\alpha+\\beta)^2 - 2\\alpha\\beta$.</li><li>Substitute the given values: $25 = (7)^2 - 2\\alpha\\beta \\implies 25 = 49 - 2\\alpha\\beta$.</li><li>Solve for the product: $2\\alpha\\beta = 49 - 25 = 24 \\implies \\alpha\\beta = 12$.</li><li>Construct the equation: $x^2 - 7x + 12 = 0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Forming a Quadratic Equation', 'Sum and Product of Roots'],
                pattern: 'Forming Equations from Conditions'
            },
            {
                id: 44,
                question: "If $\\alpha+\\beta=12$ and $\\alpha^3+\\beta^3=468$ then the quadratic equation whose roots are $\\alpha, \\beta$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Given the sum of roots $S = \\alpha+\\beta = 12$. We need the product $P=\\alpha\\beta$.</li><li>Use the identity $\\alpha^3+\\beta^3 = (\\alpha+\\beta)^3 - 3\\alpha\\beta(\\alpha+\\beta)$.</li><li>Substitute the given values: $468 = (12)^3 - 3P(12)$.</li><li>Simplify: $468 = 1728 - 36P$.</li><li>Solve for P: $36P = 1728 - 468 = 1260 \\implies P = 1260 / 36 = 35$.</li><li>Construct the equation $x^2-Sx+P=0$: $x^2-12x+35=0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Forming a Quadratic Equation', 'Sum and Product of Roots'],
                pattern: 'Forming Equations from Conditions'
            },
            {
                id: 45,
                question: "The equations $3x^2+2x-8=0$ and $2x^2-x-10=0$ have a common root. The common root is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Solve the first equation, $3x^2+2x-8=0$. Factoring gives $(3x-4)(x+2)=0$. The roots are $x=4/3$ and $x=-2$.</li><li>Solve the second equation, $2x^2-x-10=0$. Factoring gives $(2x-5)(x+2)=0$. The roots are $x=5/2$ and $x=-2$.</li><li>Compare the sets of roots to find the common value.</li><li>The common root is -2.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Factoring Quadratics'],
                pattern: 'Common Roots'
            },
            {
                id: 46,
                question: "If the equations $x^2+4ax+3=0$ and $2x^2+3ax-9=0$ have a common root, then $a=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $\\alpha$ be the common root. It must satisfy both equations:</li><li class="ml-4">$\\alpha^2+4a\\alpha+3=0$ (1)</li><li class="ml-4">$2\\alpha^2+3a\\alpha-9=0$ (2)</li><li>Eliminate the $\\alpha^2$ term. Multiply (1) by 2: $2\\alpha^2+8a\\alpha+6=0$ (3).</li><li>Subtract (2) from (3): $(8a\\alpha-3a\\alpha) + (6-(-9)) = 0 \\implies 5a\\alpha + 15 = 0$.</li><li>Solve for $\\alpha$: $5a\\alpha = -15$. Assuming $a \\neq 0$, $\\alpha = -3/a$.</li><li>Substitute this value of $\\alpha$ back into equation (1): $(-3/a)^2 + 4a(-3/a) + 3 = 0$.</li><li>Simplify and solve for a: $9/a^2 - 12 + 3 = 0 \\implies 9/a^2 = 9 \\implies a^2=1 \\implies a=\\pm 1$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Common Roots'],
                pattern: 'Common Roots'
            },
            {
                id: 47,
                question: "If $3x^2-2x+p=0$ and $6x^2-17x+12=0$ have a common root, then $p=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>First, find the roots of the complete equation, $6x^2-17x+12=0$.</li><li>Using the quadratic formula: $x = \\frac{17 \\pm \\sqrt{17^2-4(6)(12)}}{12} = \\frac{17 \\pm \\sqrt{1}}{12}$.</li><li>The roots are $x = \\frac{18}{12} = \\frac{3}{2}$ and $x = \\frac{16}{12} = \\frac{4}{3}$.</li><li>The common root must be one of these two values.</li><li class="ml-4">Case 1: If the common root is $x=3/2$, substitute it into the first equation: $3(3/2)^2 - 2(3/2) + p = 0 \\implies 27/4 - 3 + p = 0 \\implies p = -15/4$.</li><li class="ml-4">Case 2: If the common root is $x=4/3$, substitute it into the first equation: $3(4/3)^2 - 2(4/3) + p = 0 \\implies 16/3 - 8/3 + p = 0 \\implies p = -8/3$.</li><li>The possible values for p are -15/4 or -8/3.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Common Roots'],
                pattern: 'Common Roots'
            },
            {
                id: 48,
                question: "If $x^2+bx+c=0$, $x^2+cx+b=0$ $(b\\ne c)$ have a common root then $b+c=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $\\alpha$ be the common root.</li><li>Subtract the second equation from the first: $(\\alpha^2+b\\alpha+c) - (\\alpha^2+c\\alpha+b) = 0$.</li><li>Simplify: $b\\alpha-c\\alpha + c-b = 0 \\implies \\alpha(b-c) - (b-c) = 0$.</li><li>Since $b \\ne c$, we can divide by $(b-c)$ to get $\\alpha - 1 = 0$, so $\\alpha=1$.</li><li>Substitute the common root $\\alpha=1$ into the first equation: $1^2 + b(1) + c = 0$.</li><li>This gives $1+b+c=0$, so $b+c=-1$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Common Roots'],
                pattern: 'Common Roots'
            },
            {
                id: 49,
                question: "If the quadratic equations $ax^2+2cx+b=0$ and $ax^2+2bx+c=0$ $(b\\ne c)$ have a common root, then $a+4b+4c=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let $\\alpha$ be the common root.</li><li>Subtract the second equation from the first: $(ax^2+2cx+b) - (ax^2+2bx+c) = 0$.</li><li>Simplify: $2c\\alpha - 2b\\alpha + b-c = 0 \\implies 2\\alpha(c-b) - (c-b) = 0$.</li><li>Since $b \\ne c$, we can divide by $(c-b)$ to get $2\\alpha - 1 = 0$, so $\\alpha=1/2$.</li><li>Substitute the common root $\\alpha=1/2$ into the first equation: $a(1/2)^2 + 2c(1/2) + b = 0$.</li><li>Simplify: $a/4 + c + b = 0$.</li><li>Multiply by 4 to get the desired expression: $a + 4c + 4b = 0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Common Roots'],
                pattern: 'Common Roots'
            },
            {
                id: 50,
                question: "If $a>0$, then the expression $ax^2+bx+c$ is positive for all values of x provided:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The expression represents an upward-opening parabola since $a>0$.</li><li>For the expression to be always positive, the parabola must lie entirely above the x-axis.</li><li>This means the parabola cannot intersect the x-axis, which implies the equation $ax^2+bx+c=0$ has no real roots.</li><li>The condition for no real roots is a negative discriminant: $\\Delta = b^2-4ac < 0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Discriminant', 'Graph of a Quadratic Function'],
                pattern: 'Sign of a Quadratic Expression'
            },
            {
                id: 51,
                question: "If $a>0$ and $b^2-4ac<0$ then the graph $y=ax^2+bx+c$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The condition $a>0$ means the parabola opens upwards.</li><li>The condition $b^2-4ac<0$ means the discriminant is negative. This implies the equation has no real roots, so the graph never crosses the x-axis.</li><li>An upward-opening parabola that never crosses the x-axis must lie entirely above it.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Discriminant', 'Graph of a Quadratic Function'],
                pattern: 'Graph Analysis'
            },
            {
                id: 52,
                question: "If $b^2-4ac>0$ then the graph of $y=ax^2+bx+c$ where $a\\ne 0$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The condition $b^2-4ac>0$ means the discriminant is positive.</li><li>A positive discriminant means the equation $ax^2+bx+c=0$ has two distinct real roots.</li><li>The real roots of the equation are the x-intercepts of the graph.</li><li>Therefore, the graph cuts the x-axis at two distinct points.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Discriminant', 'Graph of a Quadratic Function'],
                pattern: 'Graph Analysis'
            },
            {
                id: 53,
                question: "If both the roots of $ax^2+bx+c=0$ are positive then:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Condition 1 (Real Roots): The discriminant must be non-negative, $\\Delta = b^2-4ac \\ge 0$.</li><li>Condition 2 (Positive Sum): If roots $\\alpha, \\beta$ are positive, their sum is positive. $\\alpha+\\beta = -b/a > 0$, which implies $a$ and $b$ have opposite signs ($ab<0$).</li><li>Condition 3 (Positive Product): The product of two positive roots is positive. $\\alpha\\beta = c/a > 0$, which implies $a$ and $c$ have the same sign ($ac>0$).</li><li>The combined conditions are $\\Delta \\ge 0$, $ab<0$, and $ac>0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Nature of Roots', 'Sum and Product of Roots'],
                pattern: 'Location of Roots'
            },
            {
                id: 54,
                question: "If the roots of $ax^2+bx+c=0$ are both positive and $b<0$, then:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>From the conditions for positive roots, we need the sum of roots $-b/a > 0$.</li><li>We are given $b<0$, which means $-b$ is positive.</li><li>For the fraction $-b/a$ to be positive, the denominator $a$ must also be positive. So, $a>0$.</li><li>We also need the product of roots $c/a > 0$.</li><li>Since we've established $a>0$, for this fraction to be positive, $c$ must also be positive. So, $c>0$.</li><li>Therefore, we need $a>0$ and $c>0$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Location of Roots'
            },
            {
                id: 55,
                question: "If the roots of $ax^2+bx+c=0$ are equal in magnitude but opposite in sign, then:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Let the roots be $\\alpha$ and $-\\alpha$.</li><li>Sum of roots: $\\alpha + (-\\alpha) = 0$. Since the sum is also $-b/a$, we have $-b/a = 0$, which implies $b=0$.</li><li>Product of roots: $\\alpha(-\\alpha) = -\\alpha^2$. For real roots ($\alpha \\ne 0$), this product is negative.</li><li>Since the product is also $c/a$, we have $c/a < 0$. This means $a$ and $c$ must have opposite signs.</li><li>The options which satisfy this are ($a>0, c<0$) or ($a<0, c>0$).</li></ul><p class='mt-4 font-semibold'>Conclusion: Both options (2) and (3) are possible. The question may be incomplete.</p>`,
                formulae: ['Sum and Product of Roots'],
                pattern: 'Location of Roots'
            },
            {
                id: 56,
                question: "If $x<3$ or $x>4$ then the value of $x^2-7x+12$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Factor the expression: $x^2-7x+12 = (x-3)(x-4)$.</li><li>The roots of the corresponding equation are $x=3$ and $x=4$.</li><li>The graph of $y=(x-3)(x-4)$ is an upward-opening parabola.</li><li>The parabola is above the x-axis (i.e., positive) for x-values outside the roots.</li><li>The given condition, $x<3$ or $x>4$, describes the region outside the roots.</li><li>Therefore, the expression is positive in this region.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Sign of a Quadratic Expression'],
                pattern: 'Quadratic Inequalities'
            },
            {
                id: 57,
                question: "If $x \\in R$ then the value of $x^2-6x+10$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Analyze the expression $y=x^2-6x+10$. The leading coefficient $a=1$ is positive, so it's an upward-opening parabola.</li><li>Calculate the discriminant: $\\Delta = b^2-4ac = (-6)^2 - 4(1)(10) = 36-40 = -4$.</li><li>Since the discriminant is negative and the parabola opens upwards, the graph is entirely above the x-axis.</li><li>This means the expression is always positive for all real values of x.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Discriminant', 'Sign of a Quadratic Expression'],
                pattern: 'Sign of a Quadratic Expression'
            },
            {
                id: 58,
                question: "The solution set of $x^2-5x-14>0$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>First, find the roots of $x^2-5x-14=0$.</li><li>Factoring gives $(x-7)(x+2)=0$. The roots are $x=7$ and $x=-2$.</li><li>The parabola $y=x^2-5x-14$ opens upwards.</li><li>The inequality is satisfied (the expression is positive) when x is outside the roots.</li><li>The solution is $x<-2$ or $x>7$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (1).</p>`,
                formulae: ['Sign of a Quadratic Expression'],
                pattern: 'Quadratic Inequalities'
            },
            {
                id: 59,
                question: "The solution set of $-6x^2+2x-3<0$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Analyze the expression $y=-6x^2+2x-3$. The leading coefficient $a=-6$ is negative, so it's a downward-opening parabola.</li><li>Calculate the discriminant: $\\Delta = b^2-4ac = (2)^2 - 4(-6)(-3) = 4 - 72 = -68$.</li><li>Since the discriminant is negative and the parabola opens downwards, the graph is entirely below the x-axis.</li><li>This means the expression is always negative for all real x.</li><li>The inequality asks for the values where the expression is less than 0, which is true for all real numbers.</li></ul><p class='mt-4 font-semibold'>Conclusion: The solution set is R. The correct option is (2).</p>`,
                formulae: ['Discriminant', 'Sign of a Quadratic Expression'],
                pattern: 'Quadratic Inequalities'
            },
            {
                id: 60,
                question: "The expression $-7x^2+8x-9$ is positive if x lies in:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Analyze the expression $y=-7x^2+8x-9$. The leading coefficient $a=-7$ is negative, so the parabola opens downwards.</li><li>Calculate the discriminant: $\\Delta = b^2-4ac = (8)^2 - 4(-7)(-9) = 64 - 252 = -188$.</li><li>Since the discriminant is negative and the parabola opens downwards, the expression is always negative.</li><li>There are no values of x for which the expression is positive.</li></ul><p class='mt-4 font-semibold'>Conclusion: The solution set is the empty set, $\\phi$. The correct option is (3).</p>`,
                formulae: ['Discriminant', 'Sign of a Quadratic Expression'],
                pattern: 'Quadratic Inequalities'
            },
            {
                id: 61,
                question: "The expression $x^2-x+7$ has minimum at $x=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The expression is a quadratic with $a=1 > 0$, so it has a minimum value.</li><li>The minimum occurs at the vertex, whose x-coordinate is given by $x = -\\frac{b}{2a}$.</li><li>For this expression, $a=1$ and $b=-1$.</li><li>The location of the minimum is $x = -\\frac{-1}{2(1)} = \\frac{1}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Vertex of a Parabola'],
                pattern: 'Maximum/Minimum Value'
            },
            {
                id: 62,
                question: "If $-5x^2+2x-7$ has maximum value at $x=a$ then $a=$",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The expression is a quadratic with $a=-5 < 0$, so it has a maximum value.</li><li>The maximum occurs at the vertex, whose x-coordinate is given by $x = -\\frac{b}{2a}$.</li><li>For this expression, $a=-5$ and $b=2$.</li><li>The location of the maximum is $a = x = -\\frac{2}{2(-5)} = -\\frac{2}{-10} = \\frac{1}{5}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Vertex of a Parabola'],
                pattern: 'Maximum/Minimum Value'
            },
            {
                id: 63,
                question: "The minimum value of $x^2-x$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The expression $y=x^2-x$ has $a=1 > 0$, so it has a minimum value.</li><li>First, find the x-coordinate of the vertex: $x = -\\frac{b}{2a} = -\\frac{-1}{2(1)} = \\frac{1}{2}$.</li><li>Now, substitute this x-value back into the expression to find the minimum value.</li><li>$y_{min} = (\\frac{1}{2})^2 - (\\frac{1}{2}) = \\frac{1}{4} - \\frac{1}{2} = -\\frac{1}{4}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (2).</p>`,
                formulae: ['Vertex of a Parabola'],
                pattern: 'Maximum/Minimum Value'
            },
            {
                id: 64,
                question: "The maximum value of $a^2-abx-b^2x^2$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>Rewrite the expression in standard form: $y = -b^2x^2 - abx + a^2$.</li><li>The leading coefficient is $-b^2$, which is negative (for $b \\neq 0$), so the parabola has a maximum value.</li><li>Find the x-coordinate of the vertex: $x = -\\frac{-ab}{2(-b^2)} = -\\frac{a}{2b}$.</li><li>Substitute this x-value back into the expression: $y_{max} = a^2 - ab(-\\frac{a}{2b}) - b^2(-\\frac{a}{2b})^2$.</li><li>Simplify: $y_{max} = a^2 + \\frac{a^2}{2} - b^2(\\frac{a^2}{4b^2}) = a^2 + \\frac{a^2}{2} - \\frac{a^2}{4}$.</li><li>Combine the terms: $y_{max} = \\frac{4a^2+2a^2-a^2}{4} = \\frac{5a^2}{4}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (3).</p>`,
                formulae: ['Vertex of a Parabola'],
                pattern: 'Maximum/Minimum Value'
            },
            {
                id: 65,
                question: "The minimum value of $(x-\\frac{5}{3})^2+\\frac{7}{2}$ is:",
                solution: `<ul class="list-disc list-inside space-y-2"><li>The expression is in vertex form, $y = a(x-h)^2+k$.</li><li>The term $(x-\\frac{5}{3})^2$ is a square, so its minimum possible value is 0.</li><li>This minimum occurs when $x - 5/3 = 0$, i.e., at $x=5/3$.</li><li>The minimum value of the entire expression is therefore $0 + \\frac{7}{2} = \\frac{7}{2}$.</li></ul><p class='mt-4 font-semibold'>Conclusion: The correct option is (4).</p>`,
                formulae: ['Completing the Square', 'Vertex Form'],
                pattern: 'Maximum/Minimum Value'
            }
        ];

        // --- DYNAMIC CONTENT RENDERING ---

        function renderContent() {
            const questionsContainer = document.getElementById('questions-container');
            const solutionsContainer = document.getElementById('solutions-container');
            const formulaeContainer = document.getElementById('formulae-content');
            const patternsContainer = document.getElementById('patterns-content');
            
            let questionsHTML = '';
            let solutionsHTML = '';
            let formulaeMap = new Map();
            let patternsMap = new Map();

            questionData.sort((a,b) => a.id - b.id).forEach((q) => {
                // Build Questions
                questionsHTML += `
                    <div class="p-4 border-l-4 border-blue-500 bg-blue-50 rounded">
                        <p class="font-semibold text-gray-800">Question ${q.id}: <span class="font-normal">${q.question}</span></p>
                    </div>`;

                // Build Solutions
                solutionsHTML += `
                    <div class="mb-6">
                        <div class="font-semibold text-lg text-gray-800">Question ${q.id}:</div>
                        <p class="text-gray-700 mb-3">${q.question}</p>
                        <div class="solution-toggle bg-gray-100 p-2 rounded-md inline-flex items-center gap-2 text-blue-600 font-semibold" onclick="toggleSolution('sol-${q.id}')">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z" clip-rule="evenodd" /></svg>
                            Show/Hide Solution
                        </div>
                        <div id="sol-${q.id}" class="solution-content prose mt-4">
                            ${q.solution}
                        </div>
                    </div>
                `;

                // Populate Formulae Map
                q.formulae.forEach(f => {
                    if (!formulaeMap.has(f)) formulaeMap.set(f, []);
                    formulaeMap.get(f).push(q.id);
                });

                // Populate Patterns Map
                if (!patternsMap.has(q.pattern)) patternsMap.set(q.pattern, []);
                patternsMap.get(q.pattern).push(q.id);
            });

            questionsContainer.innerHTML = questionsHTML;
            solutionsContainer.innerHTML = solutionsHTML;

            // Build Formulae HTML
            const formulaDetails = {
                'Factoring Quadratics': 'Finding two numbers that multiply to `ac` and add to `b` to split the middle term, or direct factorization for simpler cases.',
                'Difference of Squares': 'The identity $a^2 - b^2 = (a-b)(a+b)$.',
                'Complex Numbers': 'The imaginary unit $i = \\sqrt{-1}$. Complex roots of real quadratics always occur in conjugate pairs.',
                'Quadratic Formula': 'For $ax^2+bx+c=0$, roots are $x = \\frac{-b \\pm \\sqrt{b^2-4ac}}{2a}$.',
                'Sum and Product of Roots': 'For roots $\\alpha, \\beta$ of $ax^2+bx+c=0$, $\\alpha+\\beta = -b/a$ and $\\alpha\\beta = c/a$.',
                'Algebraic Identities': 'Using identities like $(\\alpha+\\beta)^2 = \\alpha^2+\\beta^2+2\\alpha\\beta$ to find symmetric functions of roots.',
                'Discriminant': 'The value $\\Delta = b^2-4ac$ determines the nature of the roots. $\\Delta > 0$ for real, distinct roots; $\\Delta = 0$ for real, equal roots; $\\Delta < 0$ for complex conjugate roots.',
                'Forming a Quadratic Equation': 'An equation with roots $\\alpha, \\beta$ is $x^2 - (\\alpha+\\beta)x + \\alpha\\beta = 0$.',
                'Rationalization': 'Multiplying the numerator and denominator by the conjugate to remove radicals from the denominator.',
                'Graph of a Quadratic Function': 'A parabola $y=ax^2+bx+c$ opens upwards if $a>0$ and downwards if $a<0$.',
                'Vertex of a Parabola': 'The turning point of the parabola, which occurs at $x = -b/(2a)$. This gives the maximum or minimum value.',
                'Substitution Method': 'Replacing a complex part of an equation (like $x^{1/3}$ or $x+1/x$) with a new variable to form a simpler quadratic equation.',
                'Laws of Indices': 'Rules for manipulating exponents, such as $x^{m/n} = \\sqrt[n]{x^m}$ and $x^{-n}=1/x^n$.',
                'Solving Radical Equations': 'Isolating a radical term and squaring both sides of the equation, remembering to check for extraneous solutions.',
                'Domain of Rational Functions': 'The denominator of a fraction cannot be zero. This creates restrictions on the possible values of x.',
                'Root of an Equation': 'A value that makes an equation true when substituted for the variable.',
                'Difference of Roots': 'The difference between roots $\\alpha$ and $\\beta$ is related to the discriminant: $(\\alpha-\\beta)^2 = \\Delta/a^2$.',
                'Transformation of Roots': 'Finding a new equation whose roots are a function of the roots of an original equation.',
                'Conjugate Roots': 'If a quadratic equation with rational coefficients has an irrational root $p+\\sqrt{q}$, it must also have the conjugate root $p-\\sqrt{q}$.',
                'Common Roots': 'Solving a system of two quadratic equations to find a value of x that satisfies both.',
                'Sign of a Quadratic Expression': 'An expression $ax^2+bx+c$ is always positive if $a>0, \\Delta<0$ and always negative if $a<0, \\Delta<0$. Otherwise, its sign depends on whether x is inside or outside the roots.',
                'Completing the Square': 'Rewriting $ax^2+bx+c$ into the vertex form $a(x-h)^2+k$.',
                'Vertex Form': 'The form $y=a(x-h)^2+k$ immediately shows the vertex at $(h,k)$ and the minimum/maximum value $k$.'
            };
            
            let formulaeHTML = '';
            const sortedFormulae = Array.from(formulaeMap.keys()).sort();

            for (let formulaName of sortedFormulae) {
                const questions = formulaeMap.get(formulaName);
                formulaeHTML += `
                    <div class="p-4 border rounded-lg">
                        <h3 class="font-semibold text-lg text-gray-800">${formulaName}</h3>
                        <div class="my-2 p-3 bg-gray-50 rounded prose">${formulaDetails[formulaName] || 'Standard definition.'}</div>
                        <p class="text-sm text-gray-600">Applied in Question(s): ${questions.sort((a,b)=>a-b).join(', ')}</p>
                    </div>
                `;
            }
            formulaeContainer.innerHTML = formulaeHTML;

            // Build Patterns HTML
            let patternsHTML = '';
            const sortedPatterns = Array.from(patternsMap.keys()).sort();
            for (let pattern of sortedPatterns) {
                const questions = patternsMap.get(pattern);
                patternsHTML += `
                    <div class="p-4 border rounded-lg">
                        <h3 class="font-semibold text-lg text-gray-800">${pattern}</h3>
                        <p class="text-sm text-gray-600 mt-1">Seen in Question(s): ${questions.sort((a,b)=>a-b).join(', ')}</p>
                    </div>
                `;
            }
            patternsContainer.innerHTML = patternsHTML;

            // Render LaTeX
             if (window.renderMathInElement) {
                renderMathInElement(document.body, {
                    delimiters: [
                        {left: '$$', right: '$$', display: true},
                        {left: '$', right: '$', display: false}
                    ],
                    throwOnError: false
                });
            }
        }

        // --- UI INTERACTIVITY ---

        function showSection(sectionId) {
            // Hide all sections
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });
            // Deactivate all nav buttons
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('active');
            });

            // Show the target section
            document.getElementById(sectionId).classList.add('active');
            // Activate the target nav button
            document.querySelector(`.nav-btn[onclick="showSection('${sectionId}')"]`).classList.add('active');
        }

        function toggleSolution(solutionId) {
            const solutionContent = document.getElementById(solutionId);
            if (solutionContent.style.display === 'block') {
                solutionContent.style.display = 'none';
            } else {
                solutionContent.style.display = 'block';
            }
        }

        // Initial render on page load
        document.addEventListener('DOMContentLoaded', renderContent);

    </script>
</body>
</html>
