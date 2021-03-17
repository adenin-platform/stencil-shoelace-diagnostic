# Stencil + Shoelace Issue Reproduction

Repo has 3 branches:
- stenciljs: uses Shoelace beta.27 built with Stencil, lazy loading works
- shoemaker: uses Shoelace beta.28 built with Shoemaker, lazy loading no longer works - manual registration of components is required
- litelement: uses Shoelace beta.33 built with LitElement (betas .29-.32 were also tested) - Stencil build fails, unclear if lazy loading would work again

Build failure in `litelement` branch is due to the following:

```bash
[ ERROR ]  TypeScript: ./node_modules/@shoelace-style/shoelace/dist/components/resize-observer/resize-observer.d.ts:9:18
           Cannot find name 'ResizeObserverEntry'.

      L8:  slResize: EventEmitter<{
      L9:      entries: ResizeObserverEntry[];
     L10:  }>;

[ ERROR ]  TypeScript: ./node_modules/@shoelace-style/shoelace/dist/components/resize-observer/resize-observer.d.ts:1:23
           Cannot find type definition file for 'resize-observer-browser'.

      L1:  /// <reference types="resize-observer-browser" />
      L2:  import { LitElement } from 'lit-element';

[45:08.2]  build failed, watching for changes... in 1.07 s
```
