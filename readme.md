# Stencil + Shoelace Issue Reproduction

Repo has 3 branches:
- stenciljs: uses Shoelace beta.27 built with Stencil, lazy loading works
- shoemaker: uses Shoelace beta.28 built with Shoemaker, lazy loading no longer works - manual registration of components is required
- litelement: uses Shoelace beta.33 built with LitElement (betas .29-.32 were also tested) - Stencil build fails, unclear if lazy loading would work again
