---
title: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
description: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player Online Stores, Kompilieren von Katalogen
- Online Stores, Kompilieren von Katalogen
- Geben Sie 1 Online Stores ein, kompilieren Sie Kataloge.
- Windows Media Player Online Stores, TSV-Dateien
- Online Stores, TSV-Dateien
- Typ 1 Online Stores, TSV-Dateien
- Windows Media Player Online Stores catcomp.exe
- Online Stores, catcomp.exe
- Geben Sie 1 Online Stores, catcomp.exe
- catcomp.exe
- Kompilieren von Katalogen
- durch Tabstopps getrennte Dateien (TSV)
- TSV-Dateien (durch Tabstopps getrennt)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341502"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Kompilieren eines vollständigen Katalogs aus TSV-Dateien

Neue Kataloge werden aus einer Reihe von TSV-Dateien (Registerkarten getrennte Werte) erstellt. Die Dateien müssen im Unicode-Format vorliegen. Platzieren Sie die unten aufgeführten erforderlichen TSV-Dateien in einem Ordner (dem Eingabe Pfad Argument für catcomp.exe), und wenden Sie catcomp.exe mithilfe der folgenden Syntax an:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Wenn keine Versionsnummer angegeben wird, wird die Versionsnummer auf 0 festgelegt. Wenn keine Gebiets Schema-ID angegeben ist, wird das Gebiets Schema des Systems verwendet. Wenn nur ein numerisches optionales Argument angegeben wird, wird davon ausgegangen, dass es sich um die Versionsnummer handelt. Wenn Debug angegeben wird, stellt die Ausgabe auf dem Bildschirm ausführlichere Diagnoseinformationen bereit.

Der folgende Code kompiliert beispielsweise einen Katalog aus den Dateien in "C: \\ CatalogData \\ 210" und gibt dem Katalog eine Versionsnummer von 210:


```C++
catcomp C:\CatalogData\210 210
```



Um ausführlichere Fehlermeldungen anzuzeigen, kann das optionale Debug-Argument wie folgt hinzugefügt werden:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Erforderliche TSV-Dateien

Jede der folgenden Dateien muss vorhanden sein, aber es kann eine leere Datei verwendet werden, wenn keine Daten für eine Datei vorhanden sind. Wenn der Katalog beispielsweise keine Funkkanäle enthält, kann radio.csv leer sein. Die Dateien müssen genau wie aufgeführt benannt werden.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Obwohl die Dateinamen über CSV-Erweiterungen verfügen müssen, sind die Dateien nicht im CSV-Format (Komma getrennte Werte) enthalten. Die Dateien müssen im TSV-Format (Tabulator getrennte Werte) vorliegen.

 

Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe drei Ausgabedateien.



| Dateiname                   | BESCHREIBUNG                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. wmdb                | Nicht komprimierter kompilierter Katalog.                                                                                                                                                      |
| Catalog. wmdb. LZ             | Katalog in komprimiertem Format. Ihr Plug-in kann den Speicherort dieser Datei an Windows Media Player in [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)übergeben. |
| kompilierte \_ eindeutige \_words.txt | Eine zwischen Ausgabedatei. Wird nicht von Windows Media Player verwendet.                                                                                                                      |



 

 

 




