---
title: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
description: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player,Kompilieren von Katalogen
- Onlineshops,Kompilieren von Katalogen
- 'Typ 1: Onlineshops,Kompilieren von Katalogen'
- Windows Media Player,TSV-Dateien
- Onlineshops, TSV-Dateien
- Geben Sie 1 Onlineshops,TSV-Dateien ein.
- Windows Media Player,catcomp.exe
- Onlineshops,catcomp.exe
- Geben Sie 1 Onlineshops ein, catcomp.exe
- catcomp.exe
- Kompilieren von Katalogen
- TSV-Dateien (Tab-Separated Value)
- TSV-Dateien (tabstopptrennte Werte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c5bc0648c19c3c8a6f9ddb819d77e48235bcd684d4911bc8a324a109c49daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863800"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Kompilieren eines vollständigen Katalogs aus TSV-Dateien

Neue Kataloge werden aus einem Satz von TSV-Dateien (Tab-Separated Value) erstellt. Die Dateien müssen im Unicode-Format vorliegen. Platzieren Sie die unten aufgeführten erforderlichen TSV-Dateien in einem Ordner (das Eingabepfadargument für catcomp.exe), und rufen Sie catcomp.exe folgenden Syntax auf:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Wenn keine Versionsnummer angegeben wird, wird die Versionsnummer auf 0 festgelegt. Wenn keine Locale ID angegeben wird, wird das System locale verwendet. Wenn nur ein numerisches optionales Argument angegeben wird, wird davon ausgegangen, dass es sich um die Versionsnummer handelt. Wenn debug angegeben ist, enthält die Ausgabe auf dem Bildschirm ausführlichere Diagnoseinformationen.

Im Folgenden wird beispielsweise ein Katalog aus den Dateien in C: CatalogData 210 kompiliert und dem Katalog die Versionsnummer \\ \\ 210 zugewiesen:


```C++
catcomp C:\CatalogData\210 210
```



Um ausführlichere Fehlermeldungen anzuzeigen, kann das optionale Debugargument wie folgt hinzugefügt werden:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Erforderliche TSV-Dateien

Jede der folgenden Dateien muss vorhanden sein, aber eine leere Datei kann verwendet werden, wenn keine Daten für eine Datei vorhanden sind. Wenn Ihr Katalog z. B. keine Radiokanäle enthält, radio.csv leer sein. Die Dateien müssen genau wie aufgeführt benannt werden.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Obwohl die Dateinamen über .csv verfügen müssen, liegen die Dateien nicht im CSV-Format (Comma Separated Values) vor. Die Dateien müssen im TSV-Format (Tab-Separated Values) vorliegen.

 

Wenn die Kompilierung erfolgreich ist, catcomp.exe drei Ausgabedateien erstellt.



| Dateiname                   | BESCHREIBUNG                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.wmdb                | Unkomprimierten kompilierten Katalog.                                                                                                                                                      |
| catalog.wmdb.lz             | Katalog im komprimierten Format. Ihr Plug-In kann den Speicherort dieser Datei Windows Media Player [IN IWMPContentPartner::GetCatalogURL speichern.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl) |
| Kompilierte \_ eindeutige \_words.txt | Eine Zwischenausgabedatei. Wird nicht von Windows Media Player.                                                                                                                      |



 

 

 




