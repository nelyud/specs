<p align="center">
  <img alt="laravel" src="https://avatars1.githubusercontent.com/u/32733112?s=70&v=4" width="70" height="70" />
</p>

## Спецификации и документация по проекту `avtocod`

![Packagist](https://img.shields.io/packagist/v/avtocod/specs.svg?style=flat&maxAge=30)
![GitHub issues](https://img.shields.io/github/issues/avtocod/specs.svg?style=flat&maxAge=30)
[![License](https://img.shields.io/packagist/l/avtocod/specs.svg)]()

---------

#### Глоссарий

* **Филд данных** (`field`) - единица информации;
* **Отчет** (`report`) - единица товара;

#### Структурные взаимосвязи

* **Отчет** - состоит из набора **филдов данных**.

### Филды данных

Филды данных обладают следующими свойствами:

* Филд имеет уникальное имя, используемое используемое как внутри системы, так и транслируемое наружу посредством отчета;
* Имена филдов являются фиксированными;
* Имя филда данных должно состоять из букв латинского алфавита в нижнем регистре;
* При необходимости разделить имя филда данных на составные слова используется символ "подчеркивания" (`_`);
* Для группировки различных филдов используется нотация с помощью точки (`.`)  (`dot notation`);
* Глубина "вложенности" нотаций может быть произвольной.

> Пример нотации с помощью точки:
>
> Имеется набор филдов: `name`, `year`, `vin`, `owner_name`. Все они относятся к базовым характеристикам транспортного средства, кроме `owner_name`, который относится к данным владельца. В этом случае их следует называть, например: `base.name`, `base.year`, `base.vin`, `owner.owner_name`.
