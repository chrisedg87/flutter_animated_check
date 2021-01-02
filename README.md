# animated_check

[![pub package](https://img.shields.io/pub/v/animated_check.svg)](https://pub.dev/packages/animated_check) 

AnimatedCheck is a Flutter package with a simple implementation of an animated checkmark icon.

![](screenshots/check_animation.gif)

## Installation

   Add this to your pubspec.yaml:
    
    dependencies:
        animated_check: ^1.0.0

## Usage

### Import

    import 'package:animated_check/animated_check.dart';

### Simple Implementation

    AnimationController(vsync: this, duration: Duration(seconds: 1));
    Animation _animation = new Tween<double>(begin: 0, end: 1)
      .animate(new CurvedAnimation(
        parent: _animationController, 
        curve: Curves.easeInOutCirc)
      );

    void _showCheck() {
      _animation.forward();
    }

    void _resetCheck() {
      _animation.reverse();
    }

    AnimatedCheck(
      progress: _animation,
      size: 200,
    )

## Contributions

All contributions are welcome!