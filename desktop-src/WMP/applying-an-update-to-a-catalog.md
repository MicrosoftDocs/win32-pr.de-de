---
title: Anwenden eines Updates auf einen Katalog
description: Anwenden eines Updates auf einen Katalog
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Online Stores, Anwenden von Updates auf Kataloge
- Online Stores, Anwenden von Updates auf Kataloge
- Typ 1 Online Stores, Anwenden von Updates auf Kataloge
- Windows Media Player Online Stores, Aktualisieren von Katalogen
- Online Stores, Kataloge aktualisieren
- Typ 1 Online Stores, Kataloge aktualisieren
- Windows Media Player Online Stores, Katalog Updates
- Online Stores, Katalog Updates
- Typ 1 Online Stores, Katalog Updates
- Katalog Updates
- Aktualisieren von Katalogen
- Anwenden von Updates auf Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339844"
---
# <a name="applying-an-update-to-a-catalog"></a>Anwenden eines Updates auf einen Katalog

> [!Note]  
> Dies erfolgt in der Regel nicht mit Ausnahme von Diagnose Zwecken – beispielsweise, um zu überprüfen, ob eine Differenz Datei gültig ist. Der auf diese Weise generierte Katalog befindet sich nicht in komprimierter Form und sollte nicht an Windows Media Player übermittelt werden.

 

Eine neue Katalog Datei kann mithilfe der unten stehenden Syntax erstellt werden, wobei *Input Catalog* der Speicherort des ursprünglichen Katalogs und *inputdiff* der Speicherort der anzuwendenden Differenz Datei ist. Die Katalogdateien müssen in unkomprimierter Form vorliegen.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Der folgende Code erstellt z. b. einen neuen Katalog aus C: \\ Catalog210 \\ catalog. wmdb und c: \\ Catalog210 \\ catalog. diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe die folgenden Ausgabedateien.



| Dateiname        | BESCHREIBUNG       |
|------------------|-------------------|
| Catalog. wmdb. New | Neue Katalog Datei. |



 

 

 




