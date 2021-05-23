<h1>Booking Controller</h1>


- <h4>Things that make it a GOOD Code :</h4>

    1- The instance of <b>BookingRepository</b> Class in constructor , that save's from making the instance in every function in which we want to use that class method.

    2- Minimum Work to controller is a very good approach.



- <h4>Things that make it a BAD Code :</h4>

    1- The value that we are getting from the <b>env</b> file is without the default value, and second for best practice is that i didn't call the env file value directly here first i call that in any custom made config file then i called that config file value here, so if i ever have to check all values that i am getting from env file i only have to look in only 1 file.

    2- we are returning the exact response that we receive from repository method we are not validating it , so that we can return the proper response e.g. ['error' => 0, 'message' => 'success', 'data' => $data].
    For this i modified the <b>index</b> method.

    3- We should have to used try catch.

    4- Instead of <b>find</b> we have to used <b>findOrFail</b> and also define the specific column name which we have to get so we avoid getting the unnecessary column.

    5- we are not validating the request with laravel validation (by request class) or any other option.

    6- we need to check for unnecessary index in request.

    7- we can minimize the lines of code in some methods by passing the request value directly as a parameter for example i modified this method <b>customerNotCall</b>.

    8- i see this type of lines in many places in our code <b>isset($data['jobid']) && $data['jobid'] != ""</b> for which i think that we can make a helper function for that and just pass the array and index name to that function which could return the boolean.