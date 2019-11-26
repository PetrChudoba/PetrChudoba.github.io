---
layout: post
title: Reduce Dependency properties boilerplate
---

## Sumary
Slightly less awfull and type-safe way to create Dependecy properties in WPF.
````csharp
public static readonly DependencyProperty LabelProperty =
    Properties.Register(x => x.Label, "Default value");
````
Instead of this monstrosity:
````csharp
public static readonly DependencyProperty LabelProperty =
    DependencyProperty.Register("Label", typeof(string), typeof(FooView), new PropertyMetadata("Default value")); 
````
Code snippets for Visual Studio included.

## Problem

