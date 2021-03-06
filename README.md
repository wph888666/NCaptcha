<p align="right">
  <span>English</span> |  
  <a href="./README_CN.md">中文</a>
</p>
<h1 align="center">NCaptcha
    <sup style="font-size:10px;">Captcha in .NET Core</sup>
</h1>

[![Build Status](https://dev.azure.com/elderjames/NCaptcha-Pipelines/_apis/build/status/ElderJames.NCaptcha?branchName=master)](https://dev.azure.com/elderjames/NCaptcha-Pipelines/_build/latest?definitionId=1&branchName=master)

## What is NCaptcha?

NCaptcha is the componentized captcha integration scheme in .NET Core that base on .NET Standard 2.0 and easy to expand.
It can help you implement security mechanism based on captcha with many out-of-the-box solutions or integrate your own implementation very easily.Because its implementation is componentized that allows you to easily implement what needs to be modified or replaced.

Components in NCaptcha are divided into "Generator","Validator","Target" and "State".
So far, session-based images, emails, and SMS solutions have been implement.

## Nuget Packages

| Package                                                                                                | NuGet Stable                                                                                                                                                                    | Downloads                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [NCaptcha](https://www.nuget.org/packages/NCaptcha/)                                                   | [![NCaptcha](https://img.shields.io/nuget/v/NCaptcha.svg)](https://www.nuget.org/packages/NCaptcha/)                                                                            | [![NCaptcha](https://img.shields.io/nuget/dt/NCaptcha.svg)](https://www.nuget.org/packages/NCaptcha/)                                                                            |
| [NCaptcha.State.Session](https://www.nuget.org/packages/NCaptcha.State.Session/)                       | [![NCaptcha.State.Session](https://img.shields.io/nuget/v/NCaptcha.State.Session.svg)](https://www.nuget.org/packages/NCaptcha.State.Session/)                                  | [![NCaptcha.State.Session](https://img.shields.io/nuget/dt/NCaptcha.State.Session.svg)](https://www.nuget.org/packages/NCaptcha.State.Session/)                                  |
| [NCaptcha.Targets.Images](https://www.nuget.org/packages/NCaptcha.Targets.Images/)                     | [![NCaptcha.Targets.Images](https://img.shields.io/nuget/v/NCaptcha.Targets.Images.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Images/)                               | [![NCaptcha.Targets.Images](https://img.shields.io/nuget/dt/NCaptcha.Targets.Images.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Images/)                               |
| [NCaptcha.Targets.Email](https://www.nuget.org/packages/NCaptcha.Targets.Email/)                       | [![NCaptcha.Targets.Email](https://img.shields.io/nuget/v/NCaptcha.Targets.Email.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Email/)                                  | [![NCaptcha.Targets.Email](https://img.shields.io/nuget/dt/NCaptcha.Targets.Email.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Email/)                                  |
| [NCaptcha.Targets.Sms](https://www.nuget.org/packages/NCaptcha.Targets.Sms/)                           | [![NCaptcha.Targets.Sms](https://img.shields.io/nuget/v/NCaptcha.Targets.Sms.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Sms/)                                        | [![NCaptcha.Targets.Sms](https://img.shields.io/nuget/dt/NCaptcha.Targets.Sms.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Sms/)                                        |
| [NCaptcha.Targets.Sms.Aliyun](https://www.nuget.org/packages/NCaptcha.Targets.Sms.Aliyun/)             | [![NCaptcha.Targets.Sms.Aliyun](https://img.shields.io/nuget/v/NCaptcha.Targets.Sms.Aliyun.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Sms.Aliyun/)                   | [![NCaptcha.Targets.Sms.Aliyun](https://img.shields.io/nuget/dt/NCaptcha.Targets.Sms.Aliyun.svg)](https://www.nuget.org/packages/NCaptcha.Targets.Sms.Aliyun/)                   |
| [NCaptcha.AspNetCore](https://www.nuget.org/packages/NCaptcha.AspNetCore/)                             | [![NCaptcha.AspNetCore](https://img.shields.io/nuget/v/NCaptcha.AspNetCore.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore/)                                           | [![NCaptcha.AspNetCore](https://img.shields.io/nuget/dt/NCaptcha.AspNetCore.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore/)                                           |
| [NCaptcha.AspNetCore.SessionImages](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionImages/) | [![NCaptcha.AspNetCore.SessionImages](https://img.shields.io/nuget/v/NCaptcha.AspNetCore.SessionImages.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionImages/) | [![NCaptcha.AspNetCore.SessionImages](https://img.shields.io/nuget/dt/NCaptcha.AspNetCore.SessionImages.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionImages/) |
| [NCaptcha.AspNetCore.SessionEmail](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionEmail/)   | [![NCaptcha.AspNetCore.SessionEmail](https://img.shields.io/nuget/v/NCaptcha.AspNetCore.SessionEmail.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionEmail/)    | [![NCaptcha.AspNetCore.SessionEmail](https://img.shields.io/nuget/dt/NCaptcha.AspNetCore.SessionEmail.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionEmail/)    |
| [NCaptcha.AspNetCore.SessionSms](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionSms/)       | [![NCaptcha.AspNetCore.SessionSms](https://img.shields.io/nuget/v/NCaptcha.AspNetCore.SessionSms.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionSms/)          | [![NCaptcha.AspNetCore.SessionSms](https://img.shields.io/nuget/dt/NCaptcha.AspNetCore.SessionSms.svg)](https://www.nuget.org/packages/NCaptcha.AspNetCore.SessionSms/)          |

## Usage

### Use out-of-the-box solutions

-   [Images captcha base on session](./docs/en/session-image.md)
-   [Email captcha base on session](./docs/en/session-email.md)
-   [Sms captcha base on session](./docs/en/session-sms.md),

    At present, the following SMS service providers have been implemented:

    -   aliyun
