---
description: In der folgenden Tabelle sind die grundlegenden Typen von benutzerdefinierten Aktionen sowie die Werte aufgeführt, die in den Feldern Typ, Quelle und Ziel der Tabelle CustomAction für jeden Typ aufgeführt sind.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Benutzerdefinierte Aktions Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5b10ffd42d2f6fecf06e0732a8960c84bea2e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868456"
---
# <a name="custom-action-types"></a>Benutzerdefinierte Aktions Typen

In der folgenden Tabelle sind die grundlegenden Typen von benutzerdefinierten Aktionen sowie die Werte aufgeführt, die in den Feldern Typ, Quelle und Ziel der Tabelle [CustomAction](customaction-table.md) für jeden Typ aufgeführt sind. Die grundlegenden benutzerdefinierten Aktionen können durch einschließen Optionaler Flagbits in die Typspalte geändert werden. Beschreibungen der Optionen und Werte finden Sie in den folgenden Abschnitten:

-   [Rückgabe Verarbeitungsoptionen für benutzerdefinierte Aktionen](custom-action-return-processing-options.md)
-   [Ausführungszeit Planungsoptionen für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md)
-   [Benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)
-   [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md)

Verwenden Sie die Links zum grundlegenden benutzerdefinierten Aktionstyp, um eine Beschreibung und die für jeden Typ verfügbaren Optionen zu erhalten.



| Grundlegender benutzerdefinierter Aktionstyp                                                                                                                           | type | `Source`                                                                                                                              | Ziel                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md) DLL-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                               | 1    | Der Schlüssel für die [binäre](binary-table.md) Tabelle.                                                                                            | Der DLL-Einstiegspunkt.                                                                                                                           |
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md) Die exe-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                               | 2    | Der Schlüssel für die [binäre](binary-table.md) Tabelle.                                                                                            | Befehlszeilen Zeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md) JScript-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                           | 5    | Der Schlüssel für die [binäre](binary-table.md) Tabelle.                                                                                            | Eine optionale JScript-Funktion, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md) VBScript-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                          | 6    | Der Schlüssel für die [binäre](binary-table.md) Tabelle.                                                                                            | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |
| [Benutzerdefinierter Aktionstyp 17](custom-action-type-17.md) DLL-Datei, die mit einem Produkt installiert wird.<br/>                                            | 17   | Schlüssel zu [Datei](file-table.md) Tabelle.                                                                                                | Der DLL-Einstiegspunkt.                                                                                                                           |
| [Benutzerdefinierter Aktionstyp 18](custom-action-type-18.md) EXE-Datei, die mit einem Produkt installiert wird.<br/>                                            | 18   | Schlüssel zu [Datei](file-table.md) Tabelle.                                                                                                | Befehlszeilen Zeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 19](custom-action-type-19.md) Zeigt eine angegebene Fehlermeldung an und gibt einen Fehler zurück, der die Installation beendet.<br/> | 19   | Leer                                                                                                                               | [Formatierte](formatted.md) Text Zeichenfolge. Die literalnachricht oder ein Index in der [Fehler](error-table.md) Tabelle.                           |
| [Benutzerdefinierter Aktionstyp 21](custom-action-type-21.md) JScript-Datei, die mit einem Produkt installiert wird.<br/>                                        | 21   | Schlüssel zu [Datei](file-table.md) Tabelle.                                                                                                | Eine optionale JScript-Funktion, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 22](custom-action-type-22.md) VBScript-Datei, die mit einem Produkt installiert wird.<br/>                                       | 22   | Schlüssel zu [Datei](file-table.md) Tabelle.                                                                                                | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |
| [Benutzerdefinierter Aktionstyp 34](custom-action-type-34.md) Die exe-Datei mit einem Pfad, der auf ein Verzeichnis verweist.<br/>                                       | 34   | Schlüssel zur [Verzeichnis](directory-table.md) Tabelle. Dies ist das Arbeitsverzeichnis für die Ausführung.                                         | Die Ziel Spalte ist [formatiert](formatted.md) und enthält den vollständigen Pfad und Namen der ausführbaren Datei, gefolgt von optionalen Argumenten. |
| [Benutzerdefinierter Aktionstyp 35](custom-action-type-35.md) Verzeichnis Satz mit formatiertem Text.<br/>                                                    | 35   | Ein Schlüssel für die [Verzeichnis](directory-table.md) Tabelle. Das angegebene Verzeichnis wird von der formatierten Zeichenfolge im Zielfeld festgelegt.   | Eine formatierte Text Zeichenfolge.                                                                                                                   |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md) In dieser Sequenz Tabelle gespeicherter JScript-Text.<br/>                                           | 37   | Null                                                                                                                                | Eine Zeichenfolge von JScript-Code.                                                                                                                  |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) VBScript-Text, der in dieser Sequenz Tabelle gespeichert ist.<br/>                                          | 38   | Null                                                                                                                                | Eine Zeichenfolge von VBScript-Code.                                                                                                                 |
| [Benutzerdefinierter Aktionstyp 50](custom-action-type-50.md) EXE-Datei mit einem Pfad, der von einem Eigenschafts Wert angegeben wird.<br/>                                 | 50   | Eigenschaftsname oder Schlüssel für [Eigenschaften](property-table.md) Tabelle.                                                                       | Befehlszeilen Zeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 51](custom-action-type-51.md) Eigenschaften Satz mit formatiertem Text.<br/>                                                     | 51   | Eigenschaftsname oder-Schlüssel für die [Eigenschaften](property-table.md) Tabelle. Diese Eigenschaft wird von der formatierten Zeichenfolge im Zielfeld festgelegt. | Eine formatierte Text Zeichenfolge.                                                                                                                   |
| [Benutzerdefinierter Aktionstyp 53](custom-action-type-53.md) Der von einem Eigenschafts Wert angegebene JScript-Text.<br/>                                           | 53   | Eigenschaftsname oder Schlüssel für [Eigenschaften](property-table.md) Tabelle.                                                                       | Eine optionale JScript-Funktion, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 54](custom-action-type-54.md) VBScript-Text, der von einem Eigenschafts Wert angegeben wird.<br/>                                          | 54   | Eigenschaftsname oder Schlüssel für [Eigenschaften](property-table.md) Tabelle.                                                                       | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |



 

Außerdem werden die folgenden benutzerdefinierten Aktions Typen für parallele Installationen verwendet:

-   [Benutzerdefinierter Aktionstyp 7](custom-action-type-7.md)
-   [Benutzerdefinierter Aktionstyp 23](custom-action-type-23.md)
-   [Benutzerdefinierter Aktionstyp 39](custom-action-type-39.md)

 

 




