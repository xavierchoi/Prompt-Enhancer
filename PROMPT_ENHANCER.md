# Prompt Enhancer Guide

## Purpose
This guide provides strategies for analyzing user prompts and enhancing them by incorporating project context, current progress, and potential requirements to create more effective development instructions.

---

## 🔍 Enhancement Process

### Step 1: Original Prompt Analysis
```markdown
[Analysis Areas]
- Intent Recognition: What does the user really want?
- Clarity Level: What parts are ambiguous?
- Scope Definition: How much work needs to be done?
- Missing Context: What information is lacking?
```

### Step 2: Project Context Collection
```markdown
[Auto-Collected Information]
- Directory structure scanning
- package.json dependency analysis
- Existing code style patterns
- Recent Git history changes
- Configuration files (tsconfig, eslint, etc.)
```

### Step 3: Potential Requirements Discovery
```markdown
[Inferred Requirements]
- Implicit prerequisites
- Related tasks
- Quality standards
- Testing needs
- Documentation requirements
```

### Step 4: Enhanced Prompt Generation
```markdown
[Enhancement Output]
- Concrete objectives
- Clear scope definition
- Step-by-step execution plan
- Explicit quality criteria
- Validation methods
```

---

## 🎯 Enhancement Patterns by Transformation Rules

### Vague → Specific
```markdown
[Input] "Fix this code"
[Analysis] 
- Unclear which file
- Ambiguous what to fix
- No defined goals

[Output] 
"Optimize performance for src/components/UserList.tsx:
- Current issue: 3-second delay when rendering 1000 items
- Target: Reduce render time to under 1 second
- Methods: Apply React.memo, virtualization, or pagination
- Preserve existing styling and API interface"
```

### Simple → Detailed Plan
```markdown
[Input] "Add search feature"
[Analysis]
- Unclear where to add
- Ambiguous search targets and methods
- Missing UI/UX considerations

[Output]
"Implement real-time search for ProductList component:

1. UI Implementation:
   - Create new SearchBar.tsx component
   - Follow UserList.tsx styling for consistency

2. Search Logic:
   - Filter by name, category, and tags
   - Apply 300ms debouncing
   - Highlight search results

3. State Management:
   - Use useState for search terms and results
   - Optimize API calls with useEffect

4. Testing:
   - Unit tests for search component
   - Performance testing with 1000 items"
```

### Feature Request → Complete Workflow
```markdown
[Input] "Create login functionality"
[Analysis]
- Authentication method unclear
- Security considerations missing
- Integration with existing system needed

[Output]
"Build comprehensive user authentication system:

Phase 1 - Backend Authentication:
- models/User.js: bcrypt password hashing
- middleware/auth.js: JWT token validation
- routes/auth.js: login/signup endpoints
- Follow existing API router patterns

Phase 2 - Frontend Implementation:
- components/LoginForm.tsx: form validation and error handling
- hooks/useAuth.js: authentication state management
- utils/authService.js: API call logic
- Reference existing UserProfile.tsx styling

Phase 3 - Security Hardening:
- Implement CSRF protection
- Add login attempt limiting
- Configure security headers

Phase 4 - Testing:
- Unit tests: per component
- Integration tests: complete auth flow
- Security tests: vulnerability verification"
```

---

## 📂 Project Context Utilization Strategies

### Existing Pattern Analysis
```markdown
[Code Style Extraction]
- Import ordering and grouping rules
- Function naming conventions
- Error handling patterns
- State management approaches
- Testing style guidelines

[Application Method]
"Following existing UserService.js patterns:
- Apply same error handling approach
- Use identical logging structure
- Maintain similar test coverage"
```

### Dependency Considerations
```markdown
[package.json Analysis]
- Libraries currently in use
- Version compatibility
- Dev/production dependency separation

[Enhancement Application]
"Leverage existing project libraries:
- Use existing fetch wrapper instead of axios
- Actively utilize lodash methods
- Minimize additional dependency introduction"
```

### Architecture Consistency
```markdown
[Structure Analysis]
- Folder structure and naming conventions
- Component hierarchy
- Data flow patterns

[Improvement Application]
"Align with src/features/ structure:
- Create features/auth/ directory
- Maintain components/, hooks/, services/ sub-structure
- Unify exports through index.js"
```

---

## 🔧 Special Situation Enhancements

### Legacy Code Improvement
```markdown
[Input] "Update this old code"
[Context Analysis]
- Existing code vintage and patterns
- Gap with current project standards
- Compatibility maintenance needs

[Enhanced Output]
"Migrate legacy/userManager.js to modern JavaScript:

1. Syntax Updates:
   - Convert var → const/let
   - Transform functions → arrow functions (where appropriate)
   - Apply Promise → async/await conversion

2. Feature Improvements:
   - Enhance error handling (add try-catch)
   - Improve type safety (JSDoc or TS)
   - Utilize current project utilities

3. Compatibility Assurance:
   - Maintain existing API interfaces
   - Minimize impact on dependent modules
   - Design for gradual migration"
```

### Emergency Bug Fixes
```markdown
[Input] "Fix this error urgently"
[Urgency Recognition + Safety Consideration]

[Enhanced Output]
"Emergency bug fix (safe hotfix approach):

🚨 Immediate Fix:
- Problem file: [analyzed filename]
- Resolve error with minimal changes
- Preserve existing logic as much as possible

⚡ Temporary Measures:
- Add fallback handling for error cases
- Enhance logging for monitoring
- Provide clear error messages to users

🔍 Follow-up Tasks (separate PR):
- Root cause analysis
- Add test cases
- Review architecture improvements"
```

---

## 📈 Automatic Quality Standards Addition

### Performance Standards
```markdown
[Auto-added to all feature development]
"Performance targets:
- Initial render: under 200ms
- User interactions: under 100ms
- Memory usage: max 20% increase from baseline
- Bundle size: under 10KB addition"
```

### Accessibility Standards
```markdown
[Auto-added for UI component work]
"Accessibility requirements:
- Proper ARIA label configuration
- Keyboard navigation support
- Maintain 4.5:1 color contrast ratio
- Screen reader compatibility testing"
```

### Testing Standards
```markdown
[Auto-added for code writing]
"Testing requirements:
- Unit tests: 100% coverage for core logic
- Integration tests: major user flows
- Edge cases: error scenario handling
- Consistency with existing test suite"
```

---

## 🤖 Enhancement Algorithm

### 1. Keyword-based Intent Recognition
```markdown
[Detection Patterns]
"fix" → debugging + improvement
"create/build" → new feature development
"optimize" → performance improvement
"refactor" → code structure improvement
"add" → feature extension
```

### 2. Context Information Priority
```markdown
[Collection Order]
1. Current working directory files
2. package.json and configuration files
3. Recent Git commit messages
4. Similar existing implementations
5. Project documentation and README
```

### 3. Standardized Output Structure
```markdown
[Enhanced Prompt Structure]
1. Clear objective statement
2. Specific work scope
3. Step-by-step execution plan
4. Quality criteria and constraints
5. Validation and testing methods
6. Related files and reference code
```

---

## 💡 Advanced Enhancement Techniques

### Implicit Requirement Discovery
```markdown
[When user says "create a button"]

[Enhanced Version]
"Develop Button component (complete UI system):

1. Base Button Component:
   - Support variants (primary, secondary, danger)
   - Size options (small, medium, large)
   - Handle disabled and loading states

2. Styling:
   - Utilize existing design system color palette
   - Style for hover, focus, active states
   - Dark mode support (if applicable)

3. Accessibility:
   - Complete ARIA attribute implementation
   - Keyboard navigation
   - Focus management

4. TypeScript Support:
   - Define Props interface
   - Type safety for event handlers

5. Storybook Documentation:
   - Various variant examples
   - Usage guidelines
   - Interaction testing"
```

### Related Task Suggestions
```markdown
[For API endpoint requests]

[Enhanced Version]
"Implement User API endpoints:

Core Tasks:
- GET /api/users (list + pagination)
- POST /api/users (user creation)
- PUT /api/users/:id (info update)
- DELETE /api/users/:id (deletion)

Related Task Suggestions:
- Auto-generate Swagger documentation
- Write API test suite
- Update frontend service layer
- Integrate permission check middleware
- Add logging and monitoring"
```

---

## 🎯 Practical Enhancement Examples

### Example 1: Vague Debugging Request
```markdown
[Original] "Why doesn't this work?"

[Analysis Process]
1. Check recently modified files
2. Estimate console errors or warnings
3. Analyze related code patterns

[Enhanced]
"Debug src/components/ProductList.tsx rendering issue:

Problem Situation:
- Expected: Product list should display
- Actual: Blank screen or error occurrence

Debugging Steps:
1. Check and analyze console error messages
2. Verify API response data structure
3. Review state management logic (useState/useEffect)
4. Examine conditional rendering logic

Resolution Priority:
1. Immediate fix: critical errors
2. Short-term improvement: enhance error handling
3. Long-term optimization: overall structure review"
```

### Example 2: Simple Feature Request
```markdown
[Original] "Add dark mode"

[Enhanced]
"Implement enterprise-wide dark mode system:

Phase 1 - Infrastructure Setup:
- Design CSS variable-based color system
- Implement theme switching Context
- Save settings to localStorage

Phase 2 - Component Application:
- Add dark mode styles to all existing components
- Priority: Header, Sidebar, main pages
- Maintain consistent color hierarchy

Phase 3 - User Experience:
- Theme toggle button (with animation)
- Auto-detect system preferences
- Smooth transition effects

Phase 4 - Quality Assurance:
- Test dark mode on all pages
- Verify accessibility contrast
- Minimize performance impact"
```

---

## 🔍 Continuous Improvement Mechanism

### Feedback Learning
```markdown
[User Feedback Pattern Analysis]
- Frequently requested modification areas
- Easy-to-miss requirements
- Effective Enhancement patterns

[Improvement Application]
- Update Enhancement algorithms
- Add new patterns
- Adjust priorities
```

### Project-specific Learning
```markdown
[Remember Project Characteristics]
- Preferred code styles
- Frequently used libraries
- Recurring work patterns
- Quality standards and constraints

[Customized Enhancement]
- Apply project-specific templates
- Reflect personalized code styles
- Suggest efficient workflows
```

This guide enables transforming even simple user requests into comprehensive, actionable prompts that maximize development productivity.