# CS231

## Errors may encounter
1. For people who use Octave 4.0 instead of Matlab, it may occur errors when submit code. [Here](https://learner.coursera.help/hc/en-us/community/posts/204693179-linear-regression-submit-error) is the solution to this problem.
replace
`str=[str str0(pos0(i)+1:pos(i)-1) sprintf('_0x%X_',str0(pos(i)))];`
by
`str=[str str0(pos0(i)+1:pos(i)-1) sprintf('_0x%X_',toascii(str0(pos(i))))];`
and replace
`str=sprintf('x0x%X_%s',char(str(1)),str(2:end));`
by
`str=sprintf('x0x%X_%s',toascii(str(1)),str(2:end));`
in both loadjson.m and makeValidFieldName.m

## What we can learn from this material
1. How to **plot trainning dataset**. Visualization should be the 1st idea when precessing data. There is a great example of how to code to visualize dataset given by **ex5**.
2. **Gradient check**. It's useful when we need varify if gradient we calculated is correct during gradient decent method. **Ex4** gives us an example of how to implement gradient checker.
3. **bsxfun**: A powerful builtin function. More details can be find [here](http://cn.mathworks.com/help/matlab/ref/bsxfun.html?requestedDomain=www.mathworks.com).
