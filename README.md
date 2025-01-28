# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common React Native bug: attempting to access component state or props before the component has fully mounted.  It provides a solution using the `useEffect` hook and explains why this approach is necessary. 

## The Problem

Accessing `this.state` or `this.props` within the `constructor` or during the initial render often results in undefined values.  This leads to unexpected behavior and runtime errors. 

## The Solution

The most effective way to solve this problem is to leverage the `useEffect` hook.  `useEffect` lets you perform side effects after the component has rendered. This ensures that the state and props are available before any attempt to access or use them.