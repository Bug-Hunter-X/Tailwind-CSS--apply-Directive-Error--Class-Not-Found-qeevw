# Tailwind CSS @apply Directive Error: Class Not Found

This repository demonstrates a common error when using Tailwind CSS's `@apply` directive: referencing a class that doesn't exist or is misspelled.  The error leads to unexpected or missing styles in the rendered HTML.

## Bug Description
The `@apply` directive injects the styles of a specified class directly into the current element's CSS. If the referenced class is not defined in your Tailwind configuration (either through default styles or custom configurations), the `@apply` directive will fail silently or throw an error (depending on your setup) and the expected styles will not be applied.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the lack of styling on the div element.  The expected background color (red) and text color (white) are missing because `bg-red-500` is misspelled as `bg-red-5000`.

## Solution
The solution is to ensure that all classes used within the `@apply` directive are correctly spelled and defined in your Tailwind configuration.  Consult your Tailwind documentation to make sure the class exists and is properly configured. The corrected code is in `bugSolution.html`

## Further Notes
This issue is specific to the use of the `@apply` directive.  Using regular class names will not produce this type of error.