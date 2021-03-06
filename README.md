# OASIS UBL Schema Validator

[![Github Actions](https://github.com/thegreenter/ubl-validator/workflows/CI/badge.svg)](https://github.com/thegreenter/ubl-validator/actions)
[![Coverage Status](https://img.shields.io/coveralls/thegreenter/ubl-validator.svg?label=coverage&style=flat-square&branch=master)](https://coveralls.io/github/thegreenter/ubl-validator?branch=master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c911fe005e73428591aa13b966bc488a)](https://www.codacy.com/manual/giansalex/ubl-validator?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=thegreenter/ubl-validator&amp;utm_campaign=Badge_Grade)  
OASIS Universal Business Language Schema Validator

## Install
Via Composer from [packagist.org](https://packagist.org/packages/greenter/ubl-validator).
```bash
composer require greenter/ubl-validator
```

## Example
```php
use Greenter\Ubl\UblValidator;

$xml = file_get_contents('20000000001-01-F001-1.xml');

$validator = new UblValidator();

if ($validator->isValid($xml)) {
  echo 'Success!!!';
} else {
  echo $validator->getError();
}
```
