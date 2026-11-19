# Portfolio Project Data — Numora - Calculator

- **Category:** `desktop-mobile` (Mobile App)
- **Category Label:** `Mobile App`
- **Accent Color:** `amber`
- **Target Assets Folder:** `public/images/projects/numora_calculator/`
- **Required Local Images:** `banner.webp`, `image01.webp`

## TypeScript Data (`ProjectCaseStudy`)

```typescript
{
  "id": "numora-calculator",
  "code": "PRO-01 // APP-01",
  "title": "Numora - Calculator",
  "category": "desktop-mobile",
  "categoryLabel": "Mobile App",
  "year": "2022",
  "status": "Completed",
  "accentColor": "amber",
  "repoUrl": "https://github.com/weztcy/Numora---Calculator",
  "license": "MIT License",
  "imageUrl": "/images/projects/numora_calculator/banner.webp",
  "images": [
    "/images/projects/numora_calculator/banner.webp"
  ],
  "summary": "A modern Android scientific calculator built with Jetpack Compose featuring a custom recursive descent parser and an AMOLED dark theme.",
  "projectDescription": "Numora Calculator delivers precision arithmetic and scientific computations through a high-performance recursive descent parser. Built natively with Jetpack Compose and Kotlin StateFlow, it pairs robust mathematical evaluation with an energy-efficient AMOLED interface for Android.",
  "architectureSummary": "Unidirectional MVVM pipeline routing Compose UI events through a ViewModel to a custom Lexer and Recursive Descent Parser via StateFlow.",
  "techStack": [
    "Kotlin",
    "Jetpack Compose",
    "Android SDK",
    "Material Design 3",
    "Coroutines",
    "StateFlow",
    "Gradle",
    "JUnit"
  ],
  "telemetryMatrix": {
    "projectType": "Native Mobile Utility",
    "targetPlatform": "Android 8.0+ (API 26 to 37)",
    "primaryDomain": "Scientific Computing",
    "architecturePipeline": "MVVM Unidirectional State Flow",
    "testingAndAudit": "Verified",
    "projectStatus": "Completed",
    "projectYear": "2022"
  },
  "desktopMobileProjectInfo": {
    "applicationType": "Native Mobile Calculator",
    "targetPlatform": "Android 8.0+ (API 26 to 37)",
    "developmentStatus": "Completed",
    "developmentYear": "2022",
    "applicationCategory": "Scientific & Utility Application"
  },
  "desktopMobileBackground": "Standard mobile calculators often compromise between basic ergonomics and scientific capability, suffering from cluttered view hierarchies or laggy equation parsing. Numora solves this by pairing a custom recursive descent mathematical engine with a responsive, reactive Jetpack Compose interface designed for distraction-free AMOLED display.",
  "desktopMobileProblemStatements": [
    {
      "title": "Cluttered Scientific Keypads",
      "description": "Traditional mobile calculator interfaces crowd advanced scientific functions onto standard screens, causing high touch error rates during ordinary arithmetic.",
      "issueCode": "ISSUE_01"
    },
    {
      "title": "Brittle Expression Parsing",
      "description": "Stock calculation tools frequently fail or crash when handling implicit multiplications, compound expressions, or nested parentheses.",
      "issueCode": "ISSUE_02"
    },
    {
      "title": "Suboptimal Display Adaptability",
      "description": "Fixed text sizing in calculator displays leads to truncated mathematical formulas or clipped output strings on long multi-step equations.",
      "issueCode": "ISSUE_03"
    }
  ],
  "desktopMobileObjectives": [
    {
      "title": "Collapsible Scientific Drawer",
      "description": "Engineer an expandable animated keypad that preserves a clean standard arithmetic mode while offering scientific tools on demand.",
      "targetTag": "TARGET_01"
    },
    {
      "title": "Deterministic Expression Engine",
      "description": "Develop a custom lexer and recursive descent parser supporting operator precedence, right-associative exponentiation, and implicit multiplication.",
      "targetTag": "TARGET_02"
    },
    {
      "title": "AMOLED Dynamic Typography",
      "description": "Implement auto-scaling display typography on a true AMOLED dark backdrop for optimal power conservation and formula readability.",
      "targetTag": "TARGET_03"
    }
  ],
  "desktopMobileFeatures": [
    {
      "title": "Advanced Lexer & Recursive Descent Parser",
      "description": "Tokenizes raw character sequences and parses arithmetic precedence, parentheses nesting, factorials, square roots, and trigonometric functions.",
      "badge": "Parser Engine",
      "metric": "100% Precedence Accuracy"
    },
    {
      "title": "Expandable Scientific Mode",
      "description": "Collapsible keypad tray revealing trigonometric functions (sin, cos, tan), power (^), factorial (!), square root, and constants (π, e).",
      "badge": "UI Transition",
      "metric": "Animated Expansion"
    },
    {
      "title": "Degrees and Radians Toggle",
      "description": "Instant runtime toggle between DEG and RAD angular units with mathematical radian conversion and tangent singularity checks.",
      "badge": "Trigonometry",
      "metric": "Dual Angular Support"
    },
    {
      "title": "AMOLED Dark Theme with Dynamic Scaling",
      "description": "High-contrast true black (#000000) layout with dynamic text size scaling that shrinks font size automatically as expression complexity grows.",
      "badge": "Ergonomics",
      "metric": "Battery-Efficient OLED"
    }
  ],
  "desktopMobileInterfaceShowcase": [
    {
      "imageUrl": "/images/projects/numora_calculator/image01.webp",
      "caption": "Interactive view showcasing standard arithmetic input and the expandable scientific panel featuring trigonometric and power functions.",
      "badge": "Dual Modes"
    }
  ],
  "desktopMobileUserFlow": {
    "summary": "Users launch the app directly into a streamlined keypad layout, entering numbers and operators that stream immediately into the state pipeline. Toggling scientific mode smoothly unfolds trigonometric, power, and constant controls, allowing complex nested evaluation with instant visual feedback and dynamic typography scaling on AMOLED displays.",
    "steps": [
      {
        "step": "01",
        "title": "Direct Launch & Expression Input",
        "description": "The user launches Numora into an immediate numeric layout and enters digits or operators without splash screen delays.",
        "actorOrNode": "User & Compose UI"
      },
      {
        "step": "02",
        "title": "Scientific Tray Expansion",
        "description": "Tapping the SCI button animates the scientific toolbar, surfacing trigonometry, power, factorial, and constants.",
        "actorOrNode": "UI Animation Layer"
      },
      {
        "step": "03",
        "title": "Angular Context Selection",
        "description": "The user switches between DEG and RAD modes to adjust trigonometric function inputs dynamically.",
        "actorOrNode": "ViewModel State"
      },
      {
        "step": "04",
        "title": "Expression Evaluation & Display",
        "description": "Tapping the equals button dispatches the string to the recursive descent engine, instantly updating the result view.",
        "actorOrNode": "Parser Engine"
      }
    ]
  },
  "desktopMobileArchitecture": {
    "summary": "Built on the Model-View-ViewModel architecture pattern, Numora decouples declarative UI components from execution logic. User actions flow through a centralized ViewModel into a custom lexer and recursive descent parser, safely emitting validated mathematical outcomes and error messages back through a single reactive StateFlow data stream.",
    "layers": [
      {
        "name": "Presentation Layer",
        "role": "Renders declarative Composable screens, handles insets, dynamic typography, and user gestures",
        "tech": "Jetpack Compose",
        "components": [
          "CalculatorScreen",
          "CalculatorDisplay",
          "CalculatorKeypad",
          "CalculatorButton"
        ]
      },
      {
        "name": "State Management Layer",
        "role": "Maintains reactive UI state, captures user intent via CalculatorAction, and emits CalculatorUiState",
        "tech": "Lifecycle ViewModel & StateFlow",
        "components": [
          "CalculatorViewModel",
          "CalculatorUiState",
          "CalculatorAction"
        ]
      },
      {
        "name": "Domain Calculation Engine",
        "role": "Performs lexical analysis, grammatical tokenization, recursive descent evaluation, and number formatting",
        "tech": "Custom Kotlin Engine",
        "components": [
          "CalculatorEngine",
          "Lexer",
          "ExpressionParser",
          "NumberFormatter"
        ]
      }
    ]
  },
  "desktopMobileDataManagement": {
    "storageType": "Ephemeral In-Memory State",
    "stateEngine": "Reactive Coroutines StateFlow",
    "offlineSyncStrategy": "Fully Standalone Offline Client",
    "cachingMechanism": "In-Memory Expression & Result State"
  },
  "desktopMobilePlatformImplementation": [
    {
      "title": "Zero-Permission Native Footprint",
      "description": "Operates completely sandboxed without requesting network, storage, or telemetry permissions in AndroidManifest.xml.",
      "badge": "Privacy & Security"
    },
    {
      "title": "WindowInsets & Edge-to-Edge Support",
      "description": "Adopts statusBarsPadding, navigationBarsPadding, and imePadding to ensure visual safety across diverse cutouts and gesture bars.",
      "badge": "System UI"
    },
    {
      "title": "Hardware Accelerated Compose Rendering",
      "description": "Utilizes Compose declarative graphics pipelines and AnimatedContent transitions for 60/120 FPS interface fluidity.",
      "badge": "Performance"
    }
  ],
  "desktopMobileTechSpecs": {
    "programmingLanguage": "Kotlin",
    "framework": "Jetpack Compose",
    "localStorage": "In-Memory StateFlow"
  },
  "desktopMobilePlatformSpecs": {
    "targetPlatform": "Android Mobile Devices",
    "packageFormat": "APK and AAB",
    "targetArchitecture": "ARM64 and x86 64",
    "buildFootprint": "Lightweight Native Build"
  }
}
```
