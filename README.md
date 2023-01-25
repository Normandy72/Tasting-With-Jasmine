# Testing Javascript with Jasmine
### unit testing
Independent checking for proper operation of the smallest testable part of an application.
* Independent: isolated from the rest of the system.
* Smallest testable: means you have to approach the all of code development from this prospective.
* Should be repeatable.

### mocking
Technique where dependency and its behavior is imitated (or faked).
* Can be done by the developer or a mocking library.
### Steps for Jasmine-based Tests
* Download and unzip Jasmine standalone into a directory.
[https://github.com/jasmine/jasmine/releases]()
* Erase everything in src and spec directories.
* Place your application code into the src directory.
* Place test code or a spec into the spec directory.
* Update SpecRunner.thml
    * Replace references to erased src and spec files with yours.
* Start Browser-sync (or whatever you use for local server) and go to the `http://.../SpecRunner.html` to have your specs run.

### Writing a Spec (test)
```
describe("My Function", function(){
    var initValue;

    beforeEach(function(){
        initValue = "someVal";
    });

    it("should not return true", function(){
        var result = someFunc(initValue);
        expect(result).not.toBe(true);
    });
});
```