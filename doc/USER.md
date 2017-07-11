## User

ePaisa PHP SDK provide you different object to communicate with ePaisa 2.0 REST API.

### register a new user
``` php
try {
    $ePaisa = new \eigitallabs\ePaisa\ePaisa('TOKEN');
    $payment = $ePaisa->createUser();
    $result = $payment->register($options);
    print_r($result);
} catch (\eigitallabs\ePaisa\Exception\ePaisaException $ex) {
    echo $ex->getMessage();
}
```
`$options` is an array and should contain all mandatory and optional fields you need to call `/user/register` api.
please refer to REST api documentation to find more information about it.