# [Hardened JS Intro](https://www.npmjs.com/package/ses)

Hardened JavaScript is highly compatible with ordinary JavaScript. Most existing JavaScript libraries can run on hardened JavaScript.

 - **Compartments** Compartments are separate execution contexts: each one has its own global object and global lexical scope.
 - **Frozen realm** Compartments share their intrinsics to avoid identity discontinuity. By freezing the intrinsics, SES protects programs from each other. By sharing the intrinsics, programs from separate compartments can recognize each other's arrays, data objects, and so on.
 - **Strict mode** SES enforces JavaScript strict mode that enhances security, for example by changing some silent failures into thrown errors.
 - **POLA (Principle of Least Authority)** By default, Compartments receive no ambient authority. They are created without host-provided APIs, (for example no fetch). Compartments can be selectively endowed with powerful arguments, globals, or modules.