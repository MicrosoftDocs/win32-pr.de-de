---
description: Die folgenden Einträge in den Spalten "Format", "Type" und "ContextData" der Tabelle "ModuleConfiguration" geben den semantischen Typ der Informationen an, die in das konfigurierbare Element ersetzt werden, das in der Name-Spalte der Tabelle angegeben ist
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Semantik Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2a0798a9ae7be3c2c0b56483707e3a09f67d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351124"
---
# <a name="semantic-types"></a>Semantik Typen

Die folgenden Einträge in den Spalten "Format", "Type" und "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md) " geben den semantischen Typ der Informationen an, die in das konfigurierbare Element ersetzt werden, das in der Name-Spalte der Tabelle angegeben ist

[Text Format Typen](text-format-types.md)



| Format | type       | ContextData                                                 | BESCHREIBUNG                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Text   |            |                                                             | Beliebiger Text. Siehe [beliebigen Texttyp](arbitrary-text-type.md).                                        |
| Text   | Enumeration       | <A>=<a>;<B>=<b>;<C>=<c> | Der aus einer Menge ausgewählte Wert. Siehe [Aufzählungstyp](enum-type.md).                                                 |
| Text   | Formatiert  |                                                             | Wert, der die Definition des formatierten Texts im Installer erfüllt. Siehe [formatierten Typ](formatted-type.md). |
| Text   | RTF        |                                                             | Eine RTF-Text Zeichenfolge. Siehe [RTF-Typ](rtf-type.md).                                                          |
| Text   | Bezeichner |                                                             | Eine Text Zeichenfolge, die einem Windows Installer [Bezeichner](identifier.md)entspricht.                              |



 

[Ganzzahlige Format Typen](integer-format-types.md)



| Format  | type | ContextData | BESCHREIBUNG                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Ein ganzzahliger Wert. Siehe [beliebigen ganzzahligen Typ](arbitrary-integer-type.md). |



 

[Schlüssel Format Typen](key-format-types.md)



| Format | type      | ContextData      | BESCHREIBUNG                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Schlüssel    | File      | Assemblycontext  | Ermöglicht es Benutzern, Fremdschlüssel für Win32-oder Common Language Runtime-Assemblys zu konfigurieren. Siehe [Dateityp](file-type.md). |
| Schlüssel    | Binary    | Bitmap           | Fremdschlüssel für eine binäre Tabellenzeile, die eine Bitmap für die Verwendung in der Benutzeroberfläche enthält. Siehe [Binary Type](binary-type.md).                  |
| Schlüssel    | Binary    | Symbol             | Fremdschlüssel für eine binäre Tabellenzeile, die ein Symbol für die Verwendung in der Benutzeroberfläche enthält. Siehe [Binary Type](binary-type.md).                   |
| Schlüssel    | Binary    | EXE              | Fremdschlüssel für eine binäre Tabellenzeile, die eine 32-Bit-exe-Datei enthält. Siehe [Binary Type](binary-type.md).                             |
| Schlüssel    | Binary    | EXE64            | Fremdschlüssel für eine binäre Tabellenzeile, die eine 32-oder 64-Bit-exe-Datei enthält. Siehe [Binary Type](binary-type.md).                       |
| Schlüssel    | Symbol      | Shortcuticon     | Fremdschlüssel für eine Symboltabellen Zeile, die ein Symbol für die Verwendung durch eine Verknüpfung enthält. Siehe [Icon Type](icon-type.md).                |
| Schlüssel    | Dialog    | Dialognext       | Fremdschlüssel für eine Dialog Feld Tabellenzeile. Siehe den [Dialog Typ](dialog-type.md).                                                 |
| Schlüssel    | Dialog    | Dialogprev       | Fremdschlüssel für eine Dialog Feld Tabellenzeile. Siehe den [Dialog Typ](dialog-type.md).                                                 |
| Schlüssel    | Verzeichnis | Isolationdir     | Fremdschlüssel für eine Verzeichnis Tabellenzeile, zu der isolierte Dateien gehören. Siehe [Verzeichnistyp](directory-type.md).            |
| Schlüssel    | Verzeichnis | ShortcutLocation | Fremdschlüssel für eine Verzeichnis Tabellenzeile, in der eine Verknüpfung installiert werden soll. Siehe [Verzeichnistyp](directory-type.md).   |
| Key    | Eigenschaft  |                  | Fremdschlüssel für eine Eigenschaften Zeile. Siehe [Eigenschaftentyp](property-type.md).                                                 |
| Key    | Eigenschaft  | Öffentlich           | Fremdschlüssel für eine Eigenschaften Zeile. Siehe [Eigenschaftentyp](property-type.md).                                                 |
| Key    | Eigenschaft  | Private          | Fremdschlüssel für eine Eigenschaften Zeile. Siehe [Eigenschaftentyp](property-type.md).                                                 |



 

[Bitfield-Format Typen](bitfield-format-types.md)



| Format   | type | ContextData                                  | BESCHREIBUNG                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bitfeld |      | <mask>;<A>=<a>;<B> = b | Ändert eine Teilmenge von Bits in einer Spalte. Siehe [beliebigen Bitfeldtyp](arbitrary-bitfield-type.md). |



 

 

 



