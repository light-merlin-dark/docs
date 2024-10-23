# Module Guide for Merlin's Private NPM Packages

This guide outlines the standards and approach for creating private NPM packages in Merlin's ecosystem.

## Project Structure

    /src
      /tests
        /data        # Test data/output directory
        *.test.ts    # Test files
      index.ts       # Main entry point
      types.ts       # TypeScript interfaces/types
      [module].ts    # Main module file
    package.json
    tsconfig.json
    .gitignore
    README.md
    Makefile

## Key Principles

1. Minimal + Robust
    - Single responsibility
    - Essential features only
    - Strong error handling
    - Type safety
    - Proper cleanup
    - Clear API surface

2. Testing Standards
    - Tests in src/tests directory
    - Test data/output in src/tests/data
    - Clear test setup/teardown
    - Test core functionality
    - Mock external dependencies
    - Verify file/resource creation
    - Clean up after tests

3. Configuration
    - TypeScript with ESM modules
    - Verdaccio private registry
    - Proper type definitions
    - Minimal dependencies
    - Clear package.json structure

## Development Process

1. Initial Setup
    - Create project structure
    - Initialize package.json with @merlin scope
    - Configure TypeScript
    - Set up test environment
    - Add Makefile for common tasks

2. Implementation
    - Create types first
    - Implement core functionality
    - Add error handling
    - Include proper logging
    - Document public API

3. Testing
    - Write comprehensive tests
    - Verify resource creation/cleanup
    - Test error conditions
    - Mock external dependencies
    - Ensure test isolation

4. Documentation
    - Clear README with examples
    - API documentation
    - Configuration options
    - Installation instructions
    - Usage examples

## Publishing

1. Package Configuration
    - Proper @merlin scope
    - Verdaccio registry
    - ESM module type
    - TypeScript declarations
    - Correct files included

2. Version Management
    - Semantic versioning
    - Version bump scripts
    - Pre-publish build
    - Clean distribution

3. Distribution
    - Build before publish
    - Verify types
    - Test before publish
    - Use Verdaccio registry

## Standards

1. Code
    - TypeScript strict mode
    - Clear error handling
    - Resource cleanup
    - Proper async/await
    - Type definitions
    - Single responsibility

2. Testing
    - Vitest framework
    - Clear test cases
    - Proper mocking
    - Resource verification
    - Cleanup after tests

3. Documentation
    - Clear README
    - Installation guide
    - Usage examples
    - API reference
    - Configuration options

4. Build/Deploy
    - Clean builds
    - Version management
    - Registry configuration
    - Publication process

## Quality Checklist

1. Code Quality
    - TypeScript strict compliance
    - Error handling
    - Resource management
    - Clear API design
    - Minimal dependencies

2. Test Quality
    - Core functionality covered
    - Error cases tested
    - Resources verified
    - Proper cleanup
    - Isolated tests

3. Documentation Quality
    - Clear installation steps
    - Usage examples
    - API documentation
    - Configuration guide
    - Error handling guide

4. Build Quality
    - Clean compilation
    - Type generation
    - Package structure
    - Publication process
    - Version management

## Maintenance

1. Version Updates
    - Semantic versioning
    - Changelog maintenance
    - Breaking changes
    - Dependency updates
    - Security patches

2. Testing
    - Regular test runs
    - Coverage maintenance
    - Test updates
    - Environment verification
    - Integration testing

3. Documentation
    - Keep examples current
    - Update API docs
    - Maintain changelog
    - Version compatibility
    - Usage guidelines

4. Dependencies
    - Regular updates
    - Security patches
    - Compatibility checks
    - Minimal footprint
    - Version pinning
