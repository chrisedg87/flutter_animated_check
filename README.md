# animated_check

[![pub package](https://img.shields.io/pub/v/animated_check.svg)](https://pub.dev/packages/animated_check)

AnimatedCheck is a Flutter package with a simple implementation of an animated checkmark icon.

![](https://github.com/chrisedg87/flutter_animated_check/raw/main/screenshots/animated_check.gif)

## Installation

   Add this to your pubspec.yaml:

    dependencies:
        animated_check: ^1.0.0

## Usage

### Import

    import 'package:animated_check/animated_check.dart';

### Simple Implementation

    _controller = AnimationController(vsync: this, duration: const Duration(seconds: 1));

    Animation _animation = Tween<double>(begin: 0, end: 1)
      .animate(CurvedAnimation(
        parent: _animationController,
        curve: Curves.easeInOutCirc)
      );

    void _showCheck() {
      _controller.forward();
    }

    void _resetCheck() {
      _controller.reverse();
    }

    AnimatedCheck(
      progress: _animation,
      size: 200,
    )

## Contributions

All contributions are welcome!