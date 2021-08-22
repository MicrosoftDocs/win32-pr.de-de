---
title: Vordefinierte MIDL- und Basistypen
description: MIDL unterstützt die folgenden Basistypen und vordefinierten Typen.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- Datentypen MIDL, vordefiniert und Basis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ecbc76b3f680f0fffbabcff38e8562475e26be8ae4ac583a78c614d1651151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067080"
---
# <a name="midl-predefined-and-base-types"></a>Vordefinierte MIDL- und Basistypen

MIDL unterstützt die folgenden Basistypen und vordefinierten Typen.



| Datentyp                                  | Beschreibung                                                                                                                                                                                             | Standardzeichen     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**Boolean**](boolean.md)                 | 8 Bits. Nicht kompatibel mit [**oleautomation-Schnittstellen;**](oleautomation.md) verwenden Sie stattdessen VARIANT \_ BOOL.                                                                                               | Ohne Vorzeichen         |
| [**Byte**](byte.md)                       | 8 Bits.                                                                                                                                                                                                 | (–) |
| [**Char**](char-idl.md)                   | 8 Bits.                                                                                                                                                                                                 | Ohne Vorzeichen         |
| [**Doppel**](double.md)                   | 64-Bit-Gleitkommazahl.                                                                                                                                                                           | (–) |
| [**Fehlerstatus \_ \_ t**](error-status-t.md) | 32-Bit-Ganzzahl ohne Vorzeichen zum Zurückgeben von Statuswerten für die Fehlerbehandlung.                                                                                                                                 | Ohne Vorzeichen         |
| [**schweben**](float.md)                     | 32-Bit-Gleitkommazahl.                                                                                                                                                                           | (–) |
| [**handle \_ t**](handle-t.md)              | Primitiver Handletyp für die Bindung.                                                                                                                                                                      | (–) |
| [**Hyper**](hyper.md)                     | 64-Bit-Ganzzahl.                                                                                                                                                                                         | Signiert           |
| [**INT**](int.md)                         | 32-Bit-Ganzzahl. Auf 16-Bit-Plattformen kann nicht in Remotefunktionen ohne einen Größenqualifizierer wie [**short,**](short.md) [**small,**](small.md) [**long oder**](long.md) [**hyper angezeigt werden.**](hyper.md) | Signiert           |
| **\_\_int8**                               | 8-Bit-Ganzzahl. Äquivalent zu **kleinem**.                                                                                                                                                                 | Signiert           |
| **\_\_int16**                              | 16-Bit-Ganzzahl. Entspricht dem **kurzen**.                                                                                                                                                                | Signiert           |
| **\_\_int32**                              | 32-Bit-Ganzzahl. Entspricht [**long**](long.md).                                                                                                                                                     | Signiert           |
| [**\_\_int3264**](--int3264.md)           | Eine ganze Zahl, die auf 32-Bit-Plattformen 32-Bit ist und auf 64-Bit-Plattformen 64-Bit ist.                                                                                                                       | Signiert           |
| [**\_\_int64**](--int64.md)               | 64-Bit-Ganzzahl. Entspricht [**Hyper**](hyper.md).                                                                                                                                                   | Signiert           |
| [**long**](long.md)                       | 32-Bit-Ganzzahl.                                                                                                                                                                                         | Signiert           |
| [**short**](short.md)                     | 16-Bt-Ganzzahl.                                                                                                                                                                                          | Signiert           |
| [**klein**](small.md)                     | 8-Bit-Ganzzahl.                                                                                                                                                                                          | Signiert           |
| [**void**](void.md)                       | Gibt an, dass die Prozedur keinen Wert zurückgibt.                                                                                                                                                   | (–) |
| **Leere \***                                | 32-Bit-Zeiger nur für Kontexthandles.                                                                                                                                                                | (–) |
| [**wchar \_ t**](wchar-t.md)                | Vordefinierter 16-Bit-Typ für Breitzeichen.                                                                                                                                                             | Ohne Vorzeichen         |



 

 

 




