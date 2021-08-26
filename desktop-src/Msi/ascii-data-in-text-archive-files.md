---
description: Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Textarchivdatei exportiert wird, entspricht die IDT-Datei dem grundlegenden Archivdateiformat.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: ASCII-Daten in Textarchivdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7fa327d19b59793862bd2c06ce814b17979e8e8a6f72d41b1af677b715b4ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078070"
---
# <a name="ascii-data-in-text-archive-files"></a>ASCII-Daten in Textarchivdateien

Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine [Textarchivdatei](text-archive-files.md)exportiert wird, entspricht die IDT-Datei dem grundlegenden [Archivdateiformat](archive-file-format.md). Wenn die Tabelle Nicht-ASCII-Informationen enthält, wird das Format der Archivdatei um Codepageinformationen erweitert.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>Textarchivdateien, die nur ASCII-Zeichen enthalten

Wenn eine Tabelle, die nur ASCII-Zeichen enthält, in eine Archivdatei exportiert wird, weist die IDT-Datei das grundlegende [Archivdateiformat auf.](archive-file-format.md) Jeder Stream in der Tabelle wird als Datei mit der Dateierweiterung IBD exportiert. Die IBD-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert. Betrachten Sie beispielsweise den Export der folgenden [Binärtabelle.](binary-table.md)



| Name  | Daten      |
|-------|-----------|
| Bücher | Books.ibd |
| Autos  | Cars.ibd  |



 

Die Verzeichnisstruktur nach dem Exportieren dieser Tabelle lautet wie folgt. Die Informationen in der Datenbanktabelle werden in Binary.idt exportiert. Die beiden Binärdatenströme werden in Book.ibd und Cars.ibd exportiert, die im Ordner Binary gespeichert sind.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Die Binary.idt-Archivdatei hat das grundlegende [Archivdateiformat](archive-file-format.md) und würde wie folgt aussehen.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>Textarchivdateien, die Nicht-ASCII-Zeichen enthalten

Wenn die Datei Nicht-ASCII-Daten enthält, wird das grundlegende [Archivdateiformat](archive-file-format.md) der IDT-Datei um Codepageinformationen erweitert. Die dritte Zeile in der IDT-Tabelle ist die numerische Codepage gefolgt vom Tabellennamen und den Namen der Primärschlüsselspalten, die durch Registerkarten getrennt sind.

> [!Note]  
> Eine IDT-Datei, die Nicht-ASCII-Informationen enthält, sollte im ASCII-Format gespeichert werden. Beispielsweise kann eine Textarchivdatei die Spalten- und Tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst sollte ASCII sein.

 

Die folgende in Französisch lokalisierte ActionText-Tabelle würde Nicht-ASCII-Informationen enthalten. Die numerische Codepage, die für französische Zeichenfolgen verwendet wird, ist 1252.



| Aktion    | BESCHREIBUNG                                  | Vorlage |
|-----------|----------------------------------------------|----------|
| WERBEEINBLENDUNGEN | Publication d'informations sur l'application |          |



 

Die exportierte Archivdatei ActionText.idt sieht wie folgt aus.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Wenn eine Textarchivdatei Nicht-ASCII-Daten enthält, enthält die Archivdatei Codepageinformationen. Archivdateien mit Codepageinformationen können nur wieder in eine Datenbank der genauen Codepage oder in eine sprachneutrale Datenbank importiert werden. Bei einer sprachneutralen Datenbank wird die Codepage auf die Codepage der Archivdatei festgelegt. Weitere Informationen dazu, wie Windows Installer Codepages behandelt, finden Sie im Abschnitt [Codepagebehandlung (Windows Installer).](code-page-handling-windows-installer-.md)

 

 

 



