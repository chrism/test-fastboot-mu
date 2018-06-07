# test-fastboot-mu

Uses exactly the same approach as the equivalent working classic application repo.

Prior to installing ember-cli-fastboot 1.1.4-beta.1 it was running fine as a brand new module unification project with latest canary Ember.

After installing there is now this stack trace

```
⇒  EMBER_CLI_MODULE_UNIFICATION=true ember serve

Build successful (8099ms) – Serving on http://localhost:4200/

Slowest Nodes (totalTime => 5% )              | Total (avg)         
----------------------------------------------+---------------------
Babel: ember-data (2)                         | 3359ms (1679 ms)    
Babel: ember-test-helpers (2)                 | 1269ms (634 ms)     
Babel: test-fastboot-mu (4)                   | 779ms (194 ms)      
Package /assets/vendor.js (1)                 | 522ms               

App is being served by FastBoot
DEBUG: -------------------------------
DEBUG: Ember      : 3.4.0-canary+fe23def0
DEBUG: Ember Data : 3.1.1
DEBUG: -------------------------------
Error: Assertion Failed: 'config' is not a recognized type
    at assert (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/@glimmer/resolver/utils/debug.js:10:1)
    at Resolver._definitiveCollection (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/@glimmer/resolver/resolver.js:112:1)
    at Resolver.identify (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/@glimmer/resolver/resolver.js:76:1)
    at Resolver.resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/@glimmer/resolver/resolver.js:104:1)
    at Class.resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/ember-resolver/resolvers/glimmer-wrapper/index.js:152:1)
    at Class.resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/ember-resolver/resolvers/fallback/index.js:15:1)
    at Class.superWrapper [as resolve] (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-utils.js:308:1)
    at _resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/container.js:814:1)
    at Registry.resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/container.js:564:1)
    at Registry.resolve (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/container.js:568:1)
    at Class.resolveRegistration (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-runtime/lib/mixins/registry_proxy.js:17:1)
    at Class.<anonymous> (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/ember-cli-fastboot/locations/none.js:16:1)
    at ComputedProperty.get (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:2536:1)
    at _get (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:1358:1)
    at _getPath (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:1405:1)
    at _get (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:1390:1)
    at Class.<anonymous> (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/@ember/object/lib/computed/computed_macros.js:249:1)
    at ComputedProperty.get (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:2536:1)
    at Object._get [as get] (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-metal.js:1358:1)
    at Class.setURL (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/addon-tree-output/ember-cli-fastboot/locations/none.js:48:1)
    at Class.superWrapper [as setURL] (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-utils.js:308:1)
    at Class.visit (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/@ember/application/instance.js:186:1)
    at buildAppInstance.then.then (/Users/username/git/test-fastboot-mu/node_modules/fastboot/src/ember-app.js:260:28)
    at tryCatcher (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/rsvp.js:200:1)
    at invokeCallback (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/rsvp.js:372:1)
    at publish (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/rsvp.js:358:1)
    at /Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/ember-testing/lib/ext/rsvp.js:14:1
    at invokeWithOnError (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/backburner.js:256:1)
    at Queue.flush (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/backburner.js:167:1)
    at DeferredActionQueues.flush (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/backburner.js:326:1)
    at Backburner._end (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/backburner.js:772:1)
    at Backburner._boundAutorunEnd (/Users/username/git/test-fastboot-mu/tmp/broccoli_merge_trees-output_path-jnu1zxvT.tmp/assets/backburner.js:484:1)
    at <anonymous>
    at process._tickCallback (internal/process/next_tick.js:118:7)
  ```
