
<p align="center">
  <a href="https://hultner.se/"><img src="https://hultner.se/img/logo/logo_black-01.svg" alt="Hultnér Technologies" align="center" width="200"></a>
</p>
<p align="center">
	<a href="https://hultner.se/" rel="nofollow" class="rich-diff-level-one">Hultnér Technologies AB</a> | <a href="https://twitter.com/ahultner" rel="nofollow" class="rich-diff-level-one">@ahultner</a> | <a href="http://alexander.hultner.se" rel="nofollow" class="rich-diff-level-one">Blog</a> | <a href="https://slides.com/hultner/foss-north-2019/fullscreen#/" rel="nofollow" class="rich-diff-level-one">Slides, foss-north 2019</a> | <a href="https://www.facebook.com/groups/nordiskpython/" rel="nofollow" class="rich-diff-level-one">Nordisk Python Community</a> | <a href="https://github.com/Hultner/Test-faster-fix-more/" rel="nofollow" class="rich-diff-level-one">GitHub</a>
	<hr>
</p>

# ⠠⠵ Test faster, fix more 
*Property based testing in Python using Hypothesis.*


## ⠠⠵ Quick Reference
```python
# Minimal usage example
@given(
    st.integers(), 
    st.integers()
)
def test_ints_are_commutative(x, y):
    assert x + y == y + x
	
# Define special edge cases with @example, 
# especially useful for regression testing
@given(st.integers(), st.integers())
@example(-1, 1)
def test_add(a, b):
    assert add(a, b) == a + b
```

## ⠠⠵ Test & Code Podcast Interview, March 27th, 2020
[**Property Based Testing in Python with Hypothesis - Alexander Hultnér**_, Episode 107_](https://testandcode.com/107)  
Hypothesis is the Python tool used for property based testing.
Hypothesis claims to combine _"human understanding of your problem domain with machine intelligence to improve the quality of your testing process while spending less time writing tests."_

In this episode Alexander Hultnér introduces us to property based testing in Python with Hypothesis.

Some topics covered:

- What is property based testing
- Thinking differently for property based testing
- Using hypothesis / property based testing in conjunction with normal testing
- Failures saved and re-run
- What parts of development/testing is best suited for hypothesis / property based testing
- Comparing function implementations
- Testing against REST APIs that use Open API / Swagger with schemathesis
- Changing the number of tests in different test environments
- System, integration, end to end, and unit tests


## ⠠⠵ PyCon Sweden, Oct 31 - Nov 1, 2019 (Stockholm)
[![Test Fast, Fix More - Property based testing with Hypothesis by Alexander Hultnér](https://i.ytimg.com/vi/MKf6KfdTems/maxresdefault.jpg)](https://www.youtube.com/watch?v=MKf6KfdTems)  
Did you ever miss that corner case bug? Maybe it was a negative integer, strange timezone conversion behaviour, off by one error or something entirely else. These subtle bugs are often hard to catch and are easily missed in test cases. You like me have probably ran into plenty of code utilising only happy path testing, only to later discover subtle bugs which are easily fixed once pointed out. This is where property based testing comes into the picture. 

In this talk I will focus on a wonderful Python library called Hypothesis but the concepts apply to other languages as well. Hypothesis is based on the same concept as the famous QuickCheck library for Haskell, which in turn have been ported a large number of languages. Hypothesis uses a wide range of input to find edge cases that you could otherwise easily miss, once it finds these cases it narrows down the input to the minimal breaking example to provide failures which are easier to understand. 

Audience level: Intermediate 

Speaker: Alexander Hultnér

- [Video](https://www.youtube.com/watch?v=MKf6KfdTems)
- [Slides](https://slides.com/hultner/pycon-se-2019/fullscreen#/)

## ⠠⠵ foss-north, April 8-9, 2019 (Gothenburg)
[**Test Fast, Fix More – Property based in Python testing with Hypothesis** (youtube video)](https://www.youtube.com/watch?v=qKHB0Xr-Yjg)
[![Speaker at Python Pizza 2020, Alexander Hultnér talks about pydantic](https://i.ytimg.com/vi/qKHB0Xr-Yjg/maxresdefault.jpg)](https://www.youtube.com/watch?v=qKHB0Xr-Yjg)  
Did you ever miss that corner case bug? Maybe it was a negative integer, strange timezone conversion behaviour, off by one error or something entirely else. These subtle bugs are often hard to catch and are easily missed in test cases. You like me have probably ran into plenty of code utilising only happy path testing, only to later discover subtle bugs which are easily fixed once pointed out. This is where property based testing comes into the picture. 

In this talk I will focus on a wonderful Python library called Hypothesis but the concepts apply to other languages as well. Hypoethesis is based on the same concept as the famous QuickCheck library for Haskell, which in turn have been ported a large number of languages. Hypothesis uses a wide range of input to find edge cases that you could otherwise easily miss, once it finds these cases it narrows down the input to the minimal breaking example to provide failures which are easier to understand.

- [Video](https://www.youtube.com/watch?v=qKHB0Xr-Yjg)
- [Slides](https://slides.com/hultner/foss-north-2019/fullscreen#/)
- [Jupyter Lab Notebook](https://github.com/Hultner/Test-faster-fix-more/blob/master/Foss-North-2019/demo.ipynb)
- [Snippets](https://github.com/Hultner/Test-faster-fix-more/blob/master/Foss-North-2019/snippets.ipynb)

## ⠠⠵ Property based testsing/Hypothesis FAQ
**What's the requirements for using Hypothesis?**   
Install it via `pip install hypothesis` check out the [quickstart guide](https://hypothesis.readthedocs.io/en/latest/quickstart.html)

**Do I need to rewrite all my tests?**  
Absolutely not, I'd encourage to use property based testing as a complement to your current testing
and start experimenting with it on critical parts.

**Is this the same thing as a fuzzer?**  
Not quite but similar concepts, I like to think of property-based testing as structured fuzzing. 


## ⠠⠵ Links
- [Hypothesis](https://hypothesis.works), [docs](https://hypothesis.readthedocs.io/en/latest/)
- [Quickcheck, Grandfather of property based testing](https://en.wikipedia.org/wiki/QuickCheck)
- [Beyond Unit Tests, Hillel Wayne, PyCon 2018](https://www.youtube.com/watch?v=MYucYon2-lk)
- [Better Testing With Less Code, Matt Bachmann, PyCon 2016](https://www.youtube.com/watch?v=jvwfDdgg93E)
- [Choosing properties for property-based testing (F#)](https://fsharpforfunandprofit.com/posts/property-based-testing-2/)
