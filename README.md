# Doing-Math-with-Python
'''
Variance and standard deviation of a list of numbers
'''
def calculate_mean (numbers):
    s = sum(numbers)
    N = len(numbers)
    mean = s/N
    
    return mean
def find_differences(numbers):
    mean = calculate_mean(numbers)
    
    # Find the differences from the mean
    diff =[]
    for num in numbers:
        diff.append(num-mean)
    return diff
def calculate_variance(numbers):
    
    # Find the list of differences
    diff = find_differences(numbers)
    
    # Find the squared differences
    squared_diff = []
    for d in diff:
        squared_diff.append(d**2) # d를 제곱해서 squared_diff에 저장 
        
    # Find the variance
    sum_squared_diff = sum(squared_diff)
    variance =sum_squared_diff/len(numbers)
    return variance
if __name__ =='__main__':
    donations = [100, 60, 70, 900, 100, 200, 500, 500, 503, 600, 1000, 1200]
    variance = calculate_variance(donations)
    print('The variance of the list of numbers is {0}'.format(variance))
    
    std = variance**0.5
    print('The standard deviation of the list of the numbers is{0}'.format(std))
==================result==========
The variance of the list of numbers is 141047.35416666666
The standard deviation of the list of the numbers is375.5627166887931
