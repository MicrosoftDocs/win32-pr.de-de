---
title: Kompilieren eines Katalog Updates aus vollständigen Katalogen
description: Kompilieren eines Katalog Updates aus vollständigen Katalogen
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player Online Stores, Kompilieren von Katalogen
- Online Stores, Kompilieren von Katalogen
- Geben Sie 1 Online Stores ein, kompilieren Sie Kataloge.
- Windows Media Player Online Stores, Katalog Updates
- Online Stores, Katalog Updates
- Typ 1 Online Stores, Katalog Updates
- Windows Media Player Online Stores, vollständige Kataloge
- Online Stores, vollständige Kataloge
- Typ 1 Online Stores, vollständige Kataloge
- Kompilieren von Katalogen
- Katalog Updates
- vollständige Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314213"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Kompilieren eines Katalog Updates aus vollständigen Katalogen

Ein Katalog Update, das die Änderungen zwischen zwei Versionen eines kompilierten Katalogs enthält, kann mithilfe der unten stehenden Syntax erstellt werden. dabei ist *path1* das Verzeichnis, das den ersten Katalog enthält, *path2* ist das Verzeichnis, das den zweiten Katalog enthält, und das Debuggen kann optional eingeschlossen werden, um detaillierte Fehlerinformationen auf dem Bildschirm anzuzeigen. Die Katalogdateien müssen in unkomprimierter Form vorliegen – der Dateiname des kompilierten Katalogs lautet catalog. wmdb anstelle von Catalog. wmdb. LZ.


```C++
catcomp diff <path1> <path2> [debug]
```



Wenn das Verzeichnis c: Catalog210 z. b. \\ \\ Version 210 eines vollständig kompilierten Katalogs enthält und C: \\ Catalog211 \\ Version 211 enthält, erstellt der folgende Befehl eine Differenz Datei, die die Änderungen zwischen den beiden Versionen enthält:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Um ausführliche Fehlerinformationen anzuzeigen, können Sie den optionalen Debug-Parameter wie folgt hinzufügen:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe die unten aufgeführten Ausgabedateien und speichert Sie in dem Verzeichnis, das den ersten Katalog enthält.



| Dateiname             | BESCHREIBUNG                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. diff          | Nicht komprimierte kompilierte Differenz Datei.                                                                                                                                                           |
| Catalog. diff. LZ       | Komprimierte Version der Katalog Update Datei. Ihr Plug-in kann den Speicherort dieser Datei an Windows Media Player in [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)übergeben. |
| Catalog. wmdb. Delta    | Zwischen Ausgabedatei. Wird nicht von Windows Media Player verwendet                                                                                                                                       |
| Catalog. wmdb. modified | Zwischen Ausgabedatei. Wird nicht von Windows Media Player verwendet                                                                                                                                       |



 

 

 




