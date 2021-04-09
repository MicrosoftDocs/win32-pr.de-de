---
title: Vordefinierte mittlere und Basis Typen
description: In der Mitte werden die folgenden Basis-und vordefinierten Typen unterstützt.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- Datentypen mittlerer l, vordefiniert und Basis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1afaa479969d65f162a9d57935aa7fbc539701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036846"
---
# <a name="midl-predefined-and-base-types"></a>Vordefinierte mittlere und Basis Typen

In der Mitte werden die folgenden Basis-und vordefinierten Typen unterstützt.



| Datentyp                                  | BESCHREIBUNG                                                                                                                                                                                             | Standard Zeichen     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**boolean**](boolean.md)                 | 8 Bits. Nicht kompatibel mit [**oleautomation**](oleautomation.md) -Schnittstellen. Verwenden Sie \_ stattdessen Variant bool.                                                                                               | Ohne Vorzeichen         |
| [**Hobby**](byte.md)                       | 8 Bits.                                                                                                                                                                                                 | (–) |
| [**Char**](char-idl.md)                   | 8 Bits.                                                                                                                                                                                                 | Ohne Vorzeichen         |
| [**Maß**](double.md)                   | 64-Bit-Gleit Komma Zahl.                                                                                                                                                                           | (–) |
| [**Fehler \_ Status \_ t**](error-status-t.md) | 32-Bit-Ganzzahl ohne Vorzeichen zum Zurückgeben von Status Werten für die Fehlerbehandlung.                                                                                                                                 | Ohne Vorzeichen         |
| [**Hafen**](float.md)                     | 32-Bit-Gleit Komma Zahl.                                                                                                                                                                           | (–) |
| [**Handle \_ t**](handle-t.md)              | Primitiver Handle-Typ für die Bindung.                                                                                                                                                                      | (–) |
| [**Hyper**](hyper.md)                     | 64-Bit-Ganzzahl.                                                                                                                                                                                         | Signiert           |
| [**INT**](int.md)                         | 32-Bit-Ganzzahl. Auf 16-Bit-Plattformen kann nicht in Remote Funktionen ohne einen Größen Qualifizierer wie [**Short**](short.md), [**Small**](small.md), [**Long**](long.md) oder [**Hyper**](hyper.md)angezeigt werden. | Signiert           |
| **\_\_int8**                               | 8-Bit-Ganzzahl. Äquivalent zu **klein**.                                                                                                                                                                 | Signiert           |
| **\_\_Int16**                              | 16-Bit-Ganzzahl. Äquivalent zu **Short**.                                                                                                                                                                | Signiert           |
| **\_\_Int32**                              | 32-Bit-Ganzzahl. Äquivalent zu [**Long**](long.md).                                                                                                                                                     | Signiert           |
| [**\_\_int3264**](--int3264.md)           | Eine ganze Zahl, die auf 32-Bit-Plattformen 32-Bit ist und 64 Bit auf 64-Bit-Plattformen ist.                                                                                                                       | Signiert           |
| [**\_\_Int64**](--int64.md)               | 64-Bit-Ganzzahl. Äquivalent zu [**Hyper**](hyper.md).                                                                                                                                                   | Signiert           |
| [**lange**](long.md)                       | 32-Bit-Ganzzahl.                                                                                                                                                                                         | Signiert           |
| [**short**](short.md)                     | 16-BT-Ganzzahl.                                                                                                                                                                                          | Signiert           |
| [**zuletzt**](small.md)                     | 8-Bit-Ganzzahl.                                                                                                                                                                                          | Signiert           |
| [**void**](void.md)                       | Gibt an, dass die Prozedur keinen Wert zurückgibt.                                                                                                                                                   | (–) |
| **Blutung \***                                | 32-Bit-Zeiger nur für Kontext Handles.                                                                                                                                                                | (–) |
| [**WCHAR \_ t**](wchar-t.md)                | vordefinierter 16-Bit-Typ für breit Zeichen.                                                                                                                                                             | Ohne Vorzeichen         |



 

 

 




