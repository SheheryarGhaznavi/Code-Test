<h1>Booking Repository</h1>


- <h4>Things that make it a GOOD Code :</h4>

    1- Only query related stuff in repository is a very good approach.



- <h4>Things that make it a BAD Code :</h4>

    1- The value that we are getting from the <b>env</b> file is without the default value, and second for best practice is that i didn't call the env file value directly here first i call that in any custom made config file then i called that config file value here, so if i ever have to check all values that i am getting from env file i only have to look in only 1 file.

    2- we should return the proper response e.g. ['error' => 0, 'message' => 'success', 'data' => $data].

    3- We should have to used try catch.

    4- Instead of <b>find</b> we have to used <b>findOrFail</b> and also define the specific column name which we have to get so we avoid getting the unnecessary column.

    5- we should used the compact function.

    6- we need to check for unnecessary index in request.

    7- we need to put array parenthesis in <b>with</b> function whenever we used more than 1 relation .

    8- whenever query is becoming bigger then put it in multiple lines.

    9- the logger line that we put in constructor , we don't need to put that line also in our methods we just have to used <b> $this->logger</b>

    10- we cant used first() after get() function because that will generate an error.

    11- there are also some syntax error in code which can came in front by using intellisense.

    12- Carbon::now()
        date('Y-m-d H:i:s')

        we used these lines multiples time on same function which is not needed we just have to call it once then save into the variable then pass variable elsewhere.