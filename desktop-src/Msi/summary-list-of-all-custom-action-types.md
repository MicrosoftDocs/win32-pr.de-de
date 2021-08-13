---
description: In der folgenden Tabelle sind die grundlegenden Typen benutzerdefinierter Aktionen aufgeführt, und es werden die Werte angezeigt, die sich in den Feldern Typ, Quelle und Ziel der CustomAction-Tabelle für jeden Typ befinden.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Benutzerdefinierte Aktionstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624305"
---
# <a name="custom-action-types"></a>Benutzerdefinierte Aktionstypen

In der folgenden Tabelle sind die grundlegenden Typen benutzerdefinierter Aktionen aufgeführt, und es werden die Werte angezeigt, die sich in den Feldern Typ, Quelle und Ziel der [CustomAction-Tabelle](customaction-table.md) für jeden Typ befinden. Die grundlegenden benutzerdefinierten Aktionen können geändert werden, indem sie optionale Flagbits in die Spalte Typ hinzufügen. Beschreibungen der Optionen und Werte finden Sie in den folgenden Themen:

-   [Optionen für die Rückgabeverarbeitung benutzerdefinierter Aktionen](custom-action-return-processing-options.md)
-   [Optionen für die Planung der Ausführung benutzerdefinierter Aktionen](custom-action-execution-scheduling-options.md)
-   [Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md)
-   [Option "Patch deinstallieren" für benutzerdefinierte Aktionen](custom-action-patch-uninstall-option.md)

Verwenden Sie die Links zum einfachen benutzerdefinierten Aktionstyp, um eine Beschreibung und die für jeden Typ verfügbaren Optionen zu erhalten.



| Grundlegender benutzerdefinierter Aktionstyp                                                                                                                           | Typ | `Source`                                                                                                                              | Ziel                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md) DLL-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                               | 1    | Schlüssel zu [Binärtabelle.](binary-table.md)                                                                                            | DLL-Einstiegspunkt.                                                                                                                           |
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md) EXE-Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                               | 2    | Schlüssel zu [Binärtabelle.](binary-table.md)                                                                                            | Befehlszeilenzeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md)JScript Datei, die in einem binären Tabellenstream gespeichert ist.<br/>                                           | 5    | Schlüssel zu [Binärtabelle.](binary-table.md)                                                                                            | Eine optionale JScript, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md) VBScript-Datei, die in einem Binärtabellenstream gespeichert ist.<br/>                                          | 6    | Schlüssel zu [Binärtabelle.](binary-table.md)                                                                                            | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |
| [Benutzerdefinierter Aktionstyp 17](custom-action-type-17.md) DLL-Datei, die mit einem Produkt installiert wird.<br/>                                            | 17   | [Schlüssel-zu-Datei-Tabelle.](file-table.md)                                                                                                | DLL-Einstiegspunkt.                                                                                                                           |
| [Benutzerdefinierter Aktionstyp 18](custom-action-type-18.md) EXE-Datei, die mit einem Produkt installiert wird.<br/>                                            | 18   | [Schlüssel-zu-Datei-Tabelle.](file-table.md)                                                                                                | Befehlszeilenzeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 19](custom-action-type-19.md) Zeigt eine angegebene Fehlermeldung an und gibt einen Fehler zurück, der die Installation beendet.<br/> | 19   | Leer                                                                                                                               | [Formatierte Textzeichenfolge.](formatted.md) Die Literalmeldung oder ein Index in der [Error-Tabelle.](error-table.md)                           |
| [Benutzerdefinierter Aktionstyp 21](custom-action-type-21.md)JScript, die mit einem Produkt installiert ist.<br/>                                        | 21   | [Schlüssel-zu-Datei-Tabelle.](file-table.md)                                                                                                | Eine optionale JScript, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 22](custom-action-type-22.md) VBScript-Datei, die mit einem Produkt installiert wird.<br/>                                       | 22   | [Schlüssel-zu-Datei-Tabelle.](file-table.md)                                                                                                | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |
| [Benutzerdefinierter Aktionstyp 34](custom-action-type-34.md) EXE-Datei mit einem Pfad, der auf ein Verzeichnis verweisen.<br/>                                       | 34   | [Schlüssel-zu-Verzeichnis-Tabelle.](directory-table.md) Dies ist das Arbeitsverzeichnis für die Ausführung.                                         | Die Spalte Target ist [formatiert und](formatted.md) enthält den vollständigen Pfad und Namen der ausführbaren Datei, gefolgt von optionalen Argumenten. |
| [Benutzerdefinierter Aktionstyp 35](custom-action-type-35.md) Verzeichnissatz mit formatiertem Text.<br/>                                                    | 35   | Ein Schlüssel für die [Directory-Tabelle.](directory-table.md) Das designierte Verzeichnis wird durch die formatierte Zeichenfolge im Feld Ziel festgelegt.   | Eine formatierte Textzeichenfolge.                                                                                                                   |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md)JScript in dieser Sequenztabelle gespeicherten Text.<br/>                                           | 37   | Null                                                                                                                                | Eine Zeichenfolge JScript Code.                                                                                                                  |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) VBScript-Text, der in dieser Sequenztabelle gespeichert ist.<br/>                                          | 38   | Null                                                                                                                                | Eine Zeichenfolge aus VBScript-Code.                                                                                                                 |
| [Benutzerdefinierter Aktionstyp 50](custom-action-type-50.md) EXE-Datei mit einem pfad, der durch einen -Eigenschaftswert angegeben wird.<br/>                                 | 50   | Eigenschaftenname oder Schlüssel der [Property-Tabelle.](property-table.md)                                                                       | Befehlszeilenzeichenfolge.                                                                                                                       |
| [Benutzerdefinierter Aktionstyp 51](custom-action-type-51.md) Eigenschaftensatz mit formatiertem Text.<br/>                                                     | 51   | Eigenschaftenname oder Schlüssel für die [Property-Tabelle.](property-table.md) Diese Eigenschaft wird durch die formatierte Zeichenfolge im Feld Ziel festgelegt. | Eine formatierte Textzeichenfolge.                                                                                                                   |
| [Benutzerdefinierter Aktionstyp 53](custom-action-type-53.md)JScript durch einen Eigenschaftswert angegebenen Text.<br/>                                           | 53   | Eigenschaftenname oder Schlüssel der [Property-Tabelle.](property-table.md)                                                                       | Eine optionale JScript, die aufgerufen werden kann.                                                                                           |
| [Benutzerdefinierter Aktionstyp 54](custom-action-type-54.md) DURCH einen Eigenschaftswert angegebener VBScript-Text.<br/>                                          | 54   | Eigenschaftenname oder Schlüssel der [Property-Tabelle.](property-table.md)                                                                       | Eine optionale VBScript-Funktion, die aufgerufen werden kann.                                                                                          |



 

Darüber hinaus werden die folgenden benutzerdefinierten Aktionstypen bei gleichzeitigen Installationen verwendet:

-   [Benutzerdefinierter Aktionstyp 7](custom-action-type-7.md)
-   [Benutzerdefinierter Aktionstyp 23](custom-action-type-23.md)
-   [Benutzerdefinierter Aktionstyp 39](custom-action-type-39.md)

 

 




