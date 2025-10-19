# DF_3 Update Summary

## Files Updated

### 1. api/ai-hint.js
**Changes:**
- ✅ Added `EXERCISE_MODE = 1` constant (line 4) for practice/exam mode toggling
- ✅ Updated differential equation from `y'' + y = e^x` to `y'' - 4y' + 4y = (e^x/x)²`
- ✅ Updated complete solution:
  - Homogeneous: `y_h = C_1*e^(2x) + C_2*x*e^(2x)` (repeated root r=2)
  - Particular: `y_p = -e^(2x)ln|x|`
  - General: `y = C_1*e^(2x) + C_2*x*e^(2x) - e^(2x)ln|x|`
- ✅ Updated all hints and progressive help sections
- ✅ Updated Hebrew solution skeleton for both practice and exam modes

### 2. index.html
**Changes:**
- ✅ Updated `latexProblem` to new equation (line 262)
- ✅ Updated `homogeneousSolution` (line 263)
- ✅ Updated `particularSolution` (line 264)
- ✅ Updated `hint1Html` with correct characteristic equation info (lines 267-275)
- ✅ Updated `hint2Html` with correct Wronskian and g(x) (lines 277-283)
- ✅ Updated `solutionDisplayLatex` (line 285)
- ✅ Updated `solutionStepsHtml` with complete new solution steps (lines 286-299)
- ✅ Updated `check` object parameters (lines 301-306):
  - `homogeneousTerms`: ['exp(2*x)', 'x*exp(2*x)']
  - `particularTerm`: 'exp(2*x)*ln(abs(x))'
  - `particularCoeff`: -1

## New Differential Equation

**Equation:** y'' - 4y' + 4y = (e^x/x)²

**Solution Method:** Variation of Parameters

**Complete Solution:**
- **Homogeneous equation:** y'' - 4y' + 4y = 0
- **Characteristic equation:** r² - 4r + 4 = (r-2)² = 0
- **Repeated root:** r = 2
- **Homogeneous solution:** y_h = C₁e^(2x) + C₂xe^(2x)
- **g(x) simplification:** g(x) = (e^x/x)² = e^(2x)/x²
- **Wronskian:** W(y₁, y₂) = e^(4x)
- **Particular solution:** y_p = -e^(2x)ln|x|
- **General solution:** y = C₁e^(2x) + C₂xe^(2x) - e^(2x)ln|x|

## Exercise Mode
Currently set to **EXERCISE_MODE = 1** (Practice Mode)
- Students will see full solution after 10 failed attempts
- To switch to exam mode: Change `EXERCISE_MODE` to 0 in api/ai-hint.js

## Verification
All changes have been applied and verified. The DF_3 directory now contains the updated equation and solution throughout both frontend (index.html) and backend (api/ai-hint.js) files.
