---
description: Eine Textarchiv Datei für eine Windows Installer Datenbank enthält die Dateinamenerweiterung. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Archivdatei Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864471"
---
# <a name="archive-file-format"></a>Archivdatei Format

Eine [Textarchiv Datei](text-archive-files.md) für eine Windows Installer Datenbank enthält die Dateinamenerweiterung. IDT. Wenn eine gesamte Datenbank in Archivdateien exportiert wird, verfügt jede Tabelle in der Datenbank über eine separate IDT-Datei. Wenn eine Tabelle eine Datenstrom Spalte enthält, wird jeder Stream in der Tabelle durch eine Datei mit der Dateinamenerweiterung ". ibd" dargestellt. Die ibd-Dateien werden in einem Ordner mit dem gleichen Namen wie die Tabelle gespeichert.

## <a name="idt-file-format"></a>IDT-Datei Format

Die IDT-Datei einer exportierten Datenbanktabelle, die nur ASCII-Zeichen enthält, weist das folgende grundlegende Format auf.

-   Die erste Zeile enthält die Namen der Tabellen Spalten, die durch Registerkarten getrennt sind.
-   Die zweite Zeile enthält die Spaltendefinitionen, die durch Registerkarten getrennt sind.
-   Wenn die Datei nur ASCII-Daten enthält, ist die dritte Zeile Tabellenname und Primärschlüssel Spaltennamen durch Registerkarten getrennt.
-   Die verbleibenden Zeilen in der Datei stellen Zeilen in der Tabelle dar, wobei die Spalten durch Registerkarten getrennt sind.

> [!Note]  
> Wenn die Datei nicht-ASCII-Daten enthält, ist die dritte Zeile die numerische Codepage, gefolgt von den Namen der Tabellennamen und der Primärschlüssel Spalten, die durch Registerkarten getrennt sind. Eine IDT-Datei, die nicht-ASCII-Informationen enthält, muss im ASCII-Format gespeichert werden. Eine Textarchiv Datei kann z. b. die Spalten-und Tabellennamen enthalten, die als UTF-8 codiert sind, aber die Archivdatei selbst muss ASCII sein. Weitere Informationen finden Sie [im Abschnitt ASCII-Daten in Text Archivdateien](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> In den speziellen [ \_ forcecodepage](-forcecodepage.md) -und [ \_ SummaryInformation](-summaryinformation.md) . IDT-Dateien werden erweiterte Formate verwendet. \_Beschreibungen ihrer Formate finden Sie in den Abschnitten "forcecodepage" und " \_ SummaryInformation".

 

## <a name="column-definitions"></a>Spaltendefinitionen

Spaltendefinitionen werden durch Zeichen angegeben.

-   Das erste Zeichen gibt den Spaltentyp an. Ein Kleinbuchstabe gibt eine Spalte an, die keine NULL-Werte zulässt, und ein Großbuchstabe gibt an, dass die Spalte NULL-Werte enthalten kann.

    | Zeichen | Bedeutung                   |
    |-----------|---------------------------|
    | s, s      | Zeichen folgen Spalte             |
    | l, l      | Lokalisierbare Zeichen folgen Spalte |
    | v, v      | Binäre Spalte             |
    | i, i      | Ganzzahlige Spalte            |

    

     

-   Das zweite Zeichen gibt die Größe der Spaltendaten an.

    > [!Note]  
    > Der Windows Installer verwendet die angegebene Spaltengröße nicht, um die Größe der Zeichenfolge zu begrenzen, die in ein Zeichen folgen Spalten Feld eingegeben werden kann. Einige Erstellungs Tools verwenden jedoch die angegebene Spaltengröße, um die Größe einer gültigen Zeichenfolge einzuschränken. Es wird empfohlen, dass Zeichen folgen, die in eine Spalte eingegeben werden, die angegebene Größen Anforderung erfüllen.

     

    

    | Spalten Definition | Bedeutung                                    |
    |-------------------|--------------------------------------------|
    | s255              | Zeichen folgen Spalte 255 Long, die keine NULL-Werte zulässt        |
    | L50               | In der lokalisierbare Zeichen folgen Spalte 50 Long |
    | I2, I2            | Kurze ganzzahlige Spalte                       |
    | I4, I4            | Lange ganzzahlige Spalte                        |

    

     

## <a name="control-character-translation"></a>Steuerzeichen Übersetzung

Durch das Exportieren einer Tabelle in eine Textarchiv Datei werden die Steuerzeichen übersetzt, um Konflikte mit Datei Trennzeichen zu vermeiden. Beim Schreiben in die IDT-Datei werden die Steuerzeichen wie folgt übersetzt.



| Steuerzeichen | Übersetzung in. IDT | Bedeutung         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Rückraum      |
| HT                | 16                  | Registerkarte             |
| LF                | 25                  | Zeilenvorschub       |
| FF                | 24                  | Formular Feed       |
| CR                | 17                  | Wagen Rücklauf |



 

 

 



