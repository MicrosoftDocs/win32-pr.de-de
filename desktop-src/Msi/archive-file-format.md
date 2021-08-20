---
description: Eine Textarchivdatei für eine Windows Installer-Datenbank enthält die Dateierweiterung IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Archivdateiformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72c7fe21b547bb5469af00dc9202d90dba3873a7ed86a6db6261a4228097a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145833"
---
# <a name="archive-file-format"></a>Archivdateiformat

Eine [Textarchivdatei für](text-archive-files.md) eine Windows Installer-Datenbank enthält die Dateierweiterung IDT. Wenn eine gesamte Datenbank in Archivdateien exportiert wird, verfügt jede Tabelle in der Datenbank über eine separate IDT-Datei. Wenn eine Tabelle eine Streamspalte enthält, wird jeder Stream in der Tabelle durch eine Datei mit der Erweiterung IBD dargestellt. Die IBD-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert.

## <a name="idt-file-format"></a>IDT-Dateiformat

Die IDT-Datei einer exportierten Datenbanktabelle, die nur ASCII-Zeichen enthält, hat das folgende grundlegende Format.

-   Die erste Zeile enthält die Tabellenspaltennamen, die durch Tabstopps getrennt sind.
-   Die zweite Zeile enthält die Spaltendefinitionen, die durch Tabstopps getrennt sind.
-   Wenn die Datei nur ASCII-Daten enthält, ist die dritte Zeile Tabellenname und Primärschlüsselspaltennamen, die durch Tabstopps getrennt sind.
-   Die verbleibenden Zeilen in der Datei stellen Zeilen in der Tabelle dar, deren Spalten durch Tabstopps getrennt sind.

> [!Note]  
> Wenn die Datei Nicht-ASCII-Daten enthält, ist die dritte Zeile die numerische Codepage, auf die der Tabellenname und die Spaltennamen des Primärschlüssels durch Tabstopps getrennt werden. Eine IDT-Datei, die Nicht-ASCII-Informationen enthält, sollte im ASCII-Format gespeichert werden. Beispielsweise kann eine Textarchivdatei die spalten- und tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst sollte ASCII sein. Weitere Informationen finden Sie [im Abschnitt ASCII-Daten in Textarchivdateien.](ascii-data-in-text-archive-files.md)

 

> [!Note]  
> Die [ \_ speziellen Dateien ForceCodepage](-forcecodepage.md) [ \_ und SummaryInformation](-summaryinformation.md) .idt verwenden erweiterte Formate. Beschreibungen ihrer Formate finden Sie in den \_ Abschnitten ForceCodepage und \_ SummaryInformation.

 

## <a name="column-definitions"></a>Spaltendefinitionen

Spaltendefinitionen werden durch Zeichen angegeben.

-   Das erste Zeichen gibt den Spaltentyp an. Ein Kleinbuchstabe gibt eine Spalte an, die keine NULL-Werte zugibt, und ein Großbuchstabe gibt an, dass die Spalte NULL-Werte enthalten kann.

    | Zeichen | Bedeutung                   |
    |-----------|---------------------------|
    | s, S      | Zeichenfolgenspalte             |
    | l, L      | Lokalisierbare Zeichenfolgenspalte |
    | v, V      | Binäre Spalte             |
    | i, I      | Ganzzahlige Spalte            |

    

     

-   Das zweite Zeichen gibt die Größe der Spaltendaten an.

    > [!Note]  
    > Der Windows Installer verwendet nicht die angegebene Spaltengröße, um die Größe der Zeichenfolge zu beschränken, die in ein Zeichenfolgenspaltenfeld eingegeben werden kann. Einige Erstellungstools verwenden jedoch die angegebene Spaltengröße, um die Größe einer gültigen Zeichenfolge zu beschränken. Es wird empfohlen, dass Zeichenfolgen, die in eine spalte eingegeben werden, die angegebene Größenanforderung erfüllen.

     

    

    | Spaltendefinition | Bedeutung                                    |
    |-------------------|--------------------------------------------|
    | s255              | Zeichenfolgenspalte, die keine NULL-Werte zuträgt, 255 long        |
    | L50               | Nullable Localizable String Column 50 long |
    | i2, I2            | Short Integer Column                       |
    | i4, I4            | Long Integer-Spalte                        |

    

     

## <a name="control-character-translation"></a>Steuerelementzeichenübersetzung

Beim Exportieren einer Tabelle in eine Textdatei werden die Steuerzeichen übersetzt, um Konflikte mit Dateitrennzeichen zu vermeiden. Beim Schreiben in die IDT-Datei werden die Steuerzeichen wie folgt übersetzt.



| Steuerzeichen | Übersetzung in IDT | Bedeutung         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Hintergrundbereich      |
| HT                | 16                  | Registerkarte             |
| LF                | 25                  | Zeilenvorschub       |
| FF                | 24                  | Seitenvorschub       |
| CR                | 17                  | Wagenrücklauf |



 

 

 



