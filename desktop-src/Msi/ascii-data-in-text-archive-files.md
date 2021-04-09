---
description: Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Textarchiv Datei exportiert wird, entspricht die IDT-Datei dem grundlegenden Archivdatei Format.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: ASCII-Daten in Text Archivdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864464"
---
# <a name="ascii-data-in-text-archive-files"></a>ASCII-Daten in Text Archivdateien

Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine [Textarchiv Datei](text-archive-files.md)exportiert wird, entspricht die IDT-Datei dem grundlegenden [Archivdatei Format](archive-file-format.md). Wenn die Tabelle nicht-ASCII-Informationen enthält, wird das Format der Archivdatei um Code Page Informationen erweitert.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Text Archivdateien, die nur ASCII-Zeichen enthalten

Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Archivdatei exportiert wird, liegt die IDT-Datei im grundlegenden [Archivdatei Format](archive-file-format.md)vor. Jeder Stream in der Tabelle wird als Datei mit der Dateinamenerweiterung ". ibd" exportiert. Die ibd-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert. Stellen Sie sich z. b. den Export der folgenden [binären](binary-table.md) Tabelle vor.



| Name  | Daten      |
|-------|-----------|
| Bücher | Bücher. ibd |
| Autos  | Cars. ibd  |



 

Die Verzeichnisstruktur nach dem Exportieren der Tabelle lautet wie folgt. Die Informationen in der Datenbanktabelle werden in Binary. IDT exportiert. Die beiden Datenströme der Binärdaten werden in "Book. ibd" und "Cars. ibd" exportiert, die im Ordner "Binary" gespeichert sind.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Die binäre IDT-Archivdatei befindet sich im grundlegenden [Archivdatei Format](archive-file-format.md) und sieht wie folgt aus.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Text Archivdateien, die nicht-ASCII-Zeichen enthalten

Wenn die Datei nicht-ASCII-Daten enthält, wird das grundlegende [Archivdatei Format](archive-file-format.md) der IDT-Datei so erweitert, dass Sie Code Page Informationen einschließt. Die dritte Zeile in der. IDT-Tabelle ist die numerische Codepage, gefolgt von den Namen der Tabellennamen und der Primärschlüssel Spalten, die durch Registerkarten getrennt sind.

> [!Note]  
> Eine IDT-Datei, die nicht-ASCII-Informationen enthält, muss im ASCII-Format gespeichert werden. Eine Textarchiv Datei kann z. b. die Spalten-und Tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst muss ASCII sein.

 

Die folgende in Französisch lokalisierte Aktions Text Tabelle enthält nicht-ASCII-Informationen. Die für französische Zeichen folgen verwendete numerische Codepage ist 1252.



| Aktion    | BESCHREIBUNG                                  | Vorlage |
|-----------|----------------------------------------------|----------|
| WERBEEINBLENDUNGEN | Veröffentlichung/Information sur l-Anwendung |          |



 

Die exportierte Archivdatei "aktiontext. IDT" lautet wie folgt.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Wenn eine Textarchiv Datei nicht-ASCII-Daten enthält, enthält die Archivdatei Code Page Informationen. Archivdateien mit Code Page Informationen können nur zurück in eine Datenbank dieser exakten Codepage oder in eine sprachneutrale Datenbank importiert werden. Bei einer sprach neutralen Datenbank wird die Codepage auf die Codepage der Archivdatei festgelegt. Weitere Informationen zur Behandlung von Codeseiten durch Windows Installer finden Sie im Abschnitt [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



