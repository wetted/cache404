To test the fix for 
https://github.com/micronaut-projects/micronaut-cache/issues/404

1. Clone [Core PR 8963](https://github.com/micronaut-projects/micronaut-core/pull/8963), which has the fix
2. Merge in all the changes from the 4.0.x branch 
3. Publish to maven local 

I already made these changes on this project
1. Add `implementation("io.micronaut:micronaut-context:4.0.2-SNAPSHOT")` to the build dependencies
2. Add `mavenLocal()` as first entry in build repositories

Run the `DefaultStringKeySerializerSpec` test. It should pass.

