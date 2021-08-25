---
title: Anwenden eines Updates auf einen Katalog
description: Anwenden eines Updates auf einen Katalog
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Onlineshops,Anwenden von Updates auf Kataloge
- Onlineshops,Anwenden von Updates auf Kataloge
- Geben Sie 1 Onlineshops ein, und wenden Sie Updates auf Kataloge an.
- Windows Media Player Onlineshops, Aktualisieren von Katalogen
- Onlineshops,Aktualisieren von Katalogen
- Geben Sie 1 Onlineshops ein, und aktualisieren Sie Kataloge.
- Windows Media Player Onlineshops, Katalogupdates
- Onlineshops, Katalogupdates
- Geben Sie 1 Onlineshops ein, Katalogupdates
- Katalogupdates
- Aktualisieren von Katalogen
- Anwenden von Updates auf Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114b5b341df1101b221a3d8227bf0526bfa32af744f1dca7b0a53ca2d7793c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124030"
---
# <a name="applying-an-update-to-a-catalog"></a>Anwenden eines Updates auf einen Katalog

> [!Note]  
> Dies erfolgt normalerweise nur zu Diagnosezwecken, z. B. um zu überprüfen, ob eine Differenzdatei gültig ist. Der auf diese Weise generierte Katalog ist nicht komprimiert und sollte nicht an Windows Media Player übergeben werden.

 

Eine neue Katalogdatei kann mithilfe der folgenden Syntax erstellt werden, wobei *inputcatalog* der Speicherort des ursprünglichen Katalogs und *inputdiff* der Speicherort der zu übernehmenden Differenzdatei ist. Die Katalogdateien müssen unkomprimiert sein.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Im Folgenden wird beispielsweise ein neuer Katalog aus C erstellt: \\ Catalog210 \\ catalog.wmdb und C: \\ Catalog210 \\ catalog.diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe die folgenden Ausgabedateien.



| Dateiname        | BESCHREIBUNG       |
|------------------|-------------------|
| catalog.wmdb.new | Neue Katalogdatei. |



 

 

 




