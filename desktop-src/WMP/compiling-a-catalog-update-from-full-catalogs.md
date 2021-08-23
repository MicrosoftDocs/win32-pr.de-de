---
title: Kompilieren eines Katalogupdates aus vollständigen Katalogen
description: Kompilieren eines Katalogupdates aus vollständigen Katalogen
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player,Kompilieren von Katalogen
- Onlineshops,Kompilieren von Katalogen
- 'Typ 1: Onlineshops,Kompilieren von Katalogen'
- Windows Media Player,Katalogupdates
- Onlineshops,Katalogupdates
- Typ 1 Onlineshops,Katalogupdates
- Windows Media Player,vollständige Kataloge
- Onlineshops,vollständige Kataloge
- Typ 1 Onlineshops,vollständige Kataloge
- Kompilieren von Katalogen
- Katalogupdates
- Vollständige Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306412d98f315a6a63aa40974b03a51a388b6db5c9e09c8d5b8907ef2cc15704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763950"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Kompilieren eines Katalogupdates aus vollständigen Katalogen

Ein Katalogupdate, das die Änderungen zwischen zwei Versionen eines kompilierten Katalogs enthält, kann mithilfe der folgenden Syntax erstellt werden. Dabei ist *path1* das Verzeichnis, das den ersten Katalog enthält, *path2* das Verzeichnis, das den zweiten Katalog enthält, und debug kann optional eingeschlossen werden, um detaillierte Fehlerinformationen auf dem Bildschirm anzuzeigen. Die Katalogdateien müssen nicht komprimiert sein. Der Dateiname des kompilierten Katalogs wäre catalog.wmdb und nicht catalog.wmdb.lz.


```C++
catcomp diff <path1> <path2> [debug]
```



Wenn das Verzeichnis C: Catalog210 beispielsweise Version 210 eines vollständig kompilierten Katalogs und \\ \\ C: \\ Catalog211 Version 211 enthält, erstellt der folgende Befehl eine Differenzdatei, die die Änderungen zwischen den beiden Versionen \\ enthält:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Um detaillierte Fehlerinformationen anzuzeigen, können Sie den optionalen Debugparameter wie folgt hinzufügen:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Wenn die Kompilierung erfolgreich catcomp.exe erstellt die unten aufgeführten Ausgabedateien und speichert sie in dem Verzeichnis, das den ersten Katalog enthält.



| Dateiname             | BESCHREIBUNG                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.diff          | Unkomprimierte kompilierte Differenzdatei.                                                                                                                                                           |
| catalog.diff.lz       | Komprimierte Version der Katalogupdatedatei. Ihr Plug-In kann den Speicherort dieser Datei Windows Media Player [IN IWMPContentPartner::GetCatalogURL speichern.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl) |
| catalog.wmdb.delta    | Zwischenausgabedatei. Nicht von Windows Media Player                                                                                                                                       |
| catalog.wmdb.modified | Zwischenausgabedatei. Nicht von Windows Media Player                                                                                                                                       |



 

 

 




