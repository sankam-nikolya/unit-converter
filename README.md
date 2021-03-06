# Unit Converter

[![Latest Stable Version](https://poser.pugx.org/jordanbrauer/unit-converter/version?format=flat-square)](https://packagist.org/packages/jordanbrauer/unit-converter)
[![Latest Unstable Version](https://poser.pugx.org/jordanbrauer/unit-converter/v/unstable?format=flat-square)](//packagist.org/packages/jordanbrauer/unit-converter)
[![Travis](https://img.shields.io/travis/jordanbrauer/unit-converter.svg?style=flat-square)](https://travis-ci.org/jordanbrauer/unit-converter)
[![Code Maintainability](https://img.shields.io/codeclimate/maintainability/jordanbrauer/unit-converter.svg?style=flat-square)](https://codeclimate.com/github/jordanbrauer/unit-converter)
[![Code Coverage](https://img.shields.io/codeclimate/coverage/jordanbrauer/unit-converter.svg?style=flat-square)](https://codeclimate.com/github/jordanbrauer/unit-converter)
[![Technical Debt](https://img.shields.io/codeclimate/tech-debt/jordanbrauer/unit-converter.svg?style=flat-square)](https://codeclimate.com/github/jordanbrauer/unit-converter/issues)

<!-- [![Maintainability](https://api.codeclimate.com/v1/badges/0b4639967df0b1578734/maintainability)](https://codeclimate.com/github/jordanbrauer/unit-converter/maintainability) -->
<!-- [![Test Coverage](https://api.codeclimate.com/v1/badges/0b4639967df0b1578734/test_coverage)](https://codeclimate.com/github/jordanbrauer/unit-converter/test_coverage) -->

[![Maintenance](https://img.shields.io/maintenance/yes/2018.svg?style=flat-square)](https://github.com/jordanbrauer/unit-converter)
[![Packagist](https://img.shields.io/packagist/dt/jordanbrauer/unit-converter.svg?style=flat-square)](https://packagist.org/packages/jordanbrauer/unit-converter)
[![PHP from Packagist](https://img.shields.io/packagist/php-v/jordanbrauer/unit-converter.svg?style=flat-square)](https://secure.php.net/releases/)
[![composer.lock available](https://poser.pugx.org/jordanbrauer/unit-converter/composerlock?format=flat-square)](https://packagist.org/packages/jordanbrauer/unit-converter)
[![license](https://img.shields.io/github/license/jordanbrauer/unit-converter.svg?style=flat-square)](https://github.com/jordanbrauer/unit-converter/blob/master/LICENSE)

<br />

Convert all kinds of standard units of measurement from one to another with this highly customizable, easy to use, lightweight PHP component.

**Table of Contents:**

1. [About the Component](#1-about-the-component)
2. [Installing the Component](#2-installing-the-component)
3. [Basic Usage](#3-basic-usage)

## 1. About the Component

This unit converter component aims to be modern and follow best practices. It also aims to be fully SI compliant (eventually...).

It supports the following types of measurement by default (support for more measurement types are on the roadmap).

- Area
- Data Transfer Rates _Coming Soon!_
- Digital Storage _Coming Soon!_
- Energy (Power)
- Frequency **_New!_**
- Fuel Economy **_New!_**
- Length
- Mass (Weight)
- Plane Angle (Rotation)
- Pressure
- Speed
- Temperature
- Time
- Volume

You also have the ability to override & customize the default units, as well as [add your own](https://github.com/jordanbrauer/unit-converter/wiki/Unit-Customization-&-Extension#adding-your-own-custom-units)!

## 2. Installing the Component

The best way to install the component is with Composer. For other supported methods, [see the wiki](https://github.com/jordanbrauer/unit-converter/wiki/Installing-the-Package) artile on installation.

```
$ composer require jordanbrauer/unit-converter
```

## 3. Basic Usage

Using the component is very easy, especially if you have used the Symfony or Laravel frameworks before.

### Quick-Start

If you'd like to skip the minutiae of this component's setup and get right down to business, you can get started by constructing a pre-configured converter via the builder object, like so,

```php
use UnitConverter\UnitConverter;

$converter = UnitConverter::createBuilder()
    ->addSimpleCalculator()
    ->addDefaultRegistry()
    ->build();
```

and use it like this,

```php
$converter->convert(1)->from("in")->to("cm"); # (float) 2.54
```

and you're done! For a more in-depth setup guide, [**check the wiki**](https://github.com/jordanbrauer/unit-converter/wiki).

### User Documentation

Setup guides, in-depth examples, tutorials, and explanations on the component for users who are looking to integrate it into their project, as-is.

[User Documentation](https://github.com/jordanbrauer/unit-converter/wiki)

### API Documentation

If you are looking to extend and hack on this component for your own project, these pages will give you insight into all about how the component works, through the awesome power of dockblocks!

[API Documentation](https://jordanbrauer.github.io/unit-converter/)
