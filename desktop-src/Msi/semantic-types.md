---
description: Die folgenden Einträge in den Spalten Format, Type und ContextData der Tabelle ModuleConfiguration geben den semantischen Informationstyp an, der in das konfigurierbare Element ersetzt wird, das in der Spalte Name dieser Tabelle angegeben ist.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Semantische Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234e5dd929991c2ec5fecbc1d2d1bda72f4fbe52
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882645"
---
# <a name="semantic-types"></a>Semantische Typen

Die folgenden Einträge in den Spalten Format, Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md) geben den semantischen Informationstyp an, der in das konfigurierbare Element ersetzt wird, das in der Spalte Name dieser Tabelle angegeben ist.

[Textformattypen](text-format-types.md)



| Format | Typ       | ContextData                                                 | BESCHREIBUNG                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Text   |            |                                                             | Beliebiger Text. Weitere Informationen [finden Sie unter Beliebiger Texttyp.](arbitrary-text-type.md)                                        |
| Text   | Enumeration       | <A>=<a>;<B>=<b>;&lt; C &gt; = &lt; c&gt; | Aus einer Menge ausgewählter Wert. Weitere Informationen [finden Sie unter Enum Type (Enum-Typ).](enum-type.md)                                                 |
| Text   | Formatiert  |                                                             | Der Wert, der der Definition von formatiertem Text im Installationsprogramm entsprochen hat. Weitere Informationen [finden Sie unter Formatted Type (Formatierter Typ).](formatted-type.md) |
| Text   | RTF        |                                                             | Eine RTF-Textzeichenfolge. Siehe [RTF-Typ](rtf-type.md).                                                          |
| Text   | Bezeichner |                                                             | Eine Textzeichenfolge, die einem Windows Installer [Identifier entspricht.](identifier.md)                              |



 

[Ganzzahlige Formattypen](integer-format-types.md)



| Format  | Typ | ContextData | Beschreibung                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Ein ganzzahliger Wert. Weitere Informationen [finden Sie unter Beliebiger ganzzahliger Typ.](arbitrary-integer-type.md) |



 

[Schlüsselformattypen](key-format-types.md)



| Format | Typ      | ContextData      | BESCHREIBUNG                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Schlüssel    | Datei      | AssemblyContext  | Ermöglichen Sie Es Benutzern, Fremdschlüssel für Win32- oder Common Language Runtime-Assemblys zu konfigurieren. Weitere Informationen [finden Sie unter Dateityp.](file-type.md) |
| Schlüssel    | Binary    | Bitmap           | Fremdschlüssel zu einer Binärtabellenzeile, die eine Bitmap für die Verwendung in der Benutzeroberfläche enthält. Weitere Informationen [finden Sie unter Binärtyp](binary-type.md).                  |
| Schlüssel    | Binary    | Symbol             | Fremdschlüssel zu einer Binärtabellenzeile mit einem Symbol für die Verwendung in der Benutzeroberfläche. Weitere Informationen [finden Sie unter Binärtyp](binary-type.md).                   |
| Schlüssel    | Binary    | EXE              | Fremdschlüssel zu einer Binärtabellenzeile, die eine 32-Bit-EXE enthält. Weitere Informationen [finden Sie unter Binärtyp](binary-type.md).                             |
| Schlüssel    | Binary    | EXE64            | Fremdschlüssel zu einer Binärtabellenzeile, die eine 32- oder 64-Bit-EXE enthält. Weitere Informationen [finden Sie unter Binärtyp](binary-type.md).                       |
| Schlüssel    | Symbol      | ShortcutIcon     | Fremdschlüssel zu einer Symboltabellenzeile, die ein Symbol für die Verwendung durch eine Verknüpfung enthält. Siehe [Symboltyp](icon-type.md).                |
| Schlüssel    | Dialog    | DialogNext       | Fremdschlüssel zu einer Zeile einer Dialogtabelle. Weitere Informationen finden [Sie unter Dialogtyp](dialog-type.md).                                                 |
| Schlüssel    | Dialog    | DialogPrev       | Fremdschlüssel zu einer Zeile einer Dialogtabelle. Weitere Informationen finden [Sie unter Dialogtyp](dialog-type.md).                                                 |
| Schlüssel    | Verzeichnis | IsolationDir     | Fremdschlüssel zu einer Verzeichnistabellenzeile, zu der isolierte Dateien gehören. Weitere Informationen [finden Sie unter Verzeichnistyp](directory-type.md).            |
| Schlüssel    | Verzeichnis | ShortcutLocation | Fremdschlüssel zu einer Verzeichnistabellenzeile, in der eine Verknüpfung installiert werden soll. Weitere Informationen [finden Sie unter Verzeichnistyp](directory-type.md).   |
| Key    | Eigenschaft  |                  | Fremdschlüssel zu einer Eigenschaftenzeile. Weitere Informationen [finden Sie unter Eigenschaftentyp](property-type.md).                                                 |
| Key    | Eigenschaft  | Öffentlich           | Fremdschlüssel zu einer Eigenschaftenzeile. Weitere Informationen [finden Sie unter Eigenschaftentyp](property-type.md).                                                 |
| Key    | Eigenschaft  | Privat          | Fremdschlüssel für eine Eigenschaftenzeile. Weitere Informationen finden Sie unter [Eigenschaftentyp.](property-type.md)                                                 |



 

[Bitfield-Formattypen](bitfield-format-types.md)



| Format   | Typ | ContextData                                  | Beschreibung                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bitfield |      | &lt;mask &gt; ; <A> = <a> ; <B> =b | Ändert eine Teilmenge von Bits in einer Spalte. Weitere Informationen finden Sie unter [Beliebiger Bitfield-Typ.](arbitrary-bitfield-type.md) |



 

 

 



