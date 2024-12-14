# Next.js 15 Dynamic Font Import Bug

This repository demonstrates a bug in Next.js 15 related to font loading when using the `next/font` API with dynamically imported components. The font may fail to load if the import happens after the initial hydration.

## Bug Description

When a component that uses `next/font` for custom font loading is dynamically imported (e.g., using Suspense or lazy loading), the font might not be applied, resulting in the default system font being used instead. This is due to the timing of the dynamic import. 

## Solution

The solution involves ensuring that the font loading is handled properly within the context of dynamic imports, potentially involving a more robust loading mechanism or ensuring the font loads before the component is rendered.