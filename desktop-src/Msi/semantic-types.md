---
description: Die folgenden Einträge in den Spalten Format, Type und ContextData der Tabelle ModuleConfiguration geben den semantischen Informationstyp an, der durch das konfigurierbare Element ersetzt wird, das in der Spalte Name dieser Tabelle angegeben ist.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Semantische Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01845bd7790f618794816182bb4b11fc0d13baf9216d17bbd15c63a390a52a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040300"
---
# <a name="semantic-types"></a>Semantische Typen

Die folgenden Einträge in den Spalten Format, Type und ContextData der [Tabelle ModuleConfiguration](moduleconfiguration-table.md) geben den semantischen Informationstyp an, der durch das konfigurierbare Element ersetzt wird, das in der Spalte Name dieser Tabelle angegeben ist.

[Textformattypen](text-format-types.md)



| Format | type       | ContextData                                                 | BESCHREIBUNG                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Text   |            |                                                             | Beliebiger Text. Weitere Informationen finden Sie unter [Beliebiger Texttyp.](arbitrary-text-type.md)                                        |
| Text   | Enumeration       | <A>=<a>;<B>=<b>;<C>=<c> | Aus einem Satz ausgewählter Wert. Weitere Informationen finden Sie unter [Enumerationstyp.](enum-type.md)                                                 |
| Text   | Formatiert  |                                                             | Wert, der der Definition von Formatierter Text im Installationsprogramm gerecht wird. Weitere Informationen finden Sie unter [Formatierter Typ.](formatted-type.md) |
| Text   | RTF        |                                                             | Eine RTF-Textzeichenfolge. Weitere Informationen finden Sie unter [RTF-Typ.](rtf-type.md)                                                          |
| Text   | Bezeichner |                                                             | Eine Textzeichenfolge, die einem Windows [Installer-Bezeichner](identifier.md)entspricht.                              |



 

[Ganzzahlformattypen](integer-format-types.md)



| Format  | type | ContextData | BESCHREIBUNG                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Ein ganzzahliger Wert. Weitere Informationen finden Sie unter [Beliebiger ganzzahliger Typ.](arbitrary-integer-type.md) |



 

[Schlüsselformattypen](key-format-types.md)



| Format | type      | ContextData      | BESCHREIBUNG                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Schlüssel    | Datei      | AssemblyContext  | Ermöglichen Sie Es Benutzern, Fremdschlüssel für Win32- oder Common Language Runtime-Assemblys zu konfigurieren. Weitere Informationen finden Sie unter [Dateityp.](file-type.md) |
| Key    | Binary    | Bitmap           | Fremdschlüssel zu einer Binärtabellenzeile, die eine Bitmap für die Verwendung auf der Benutzeroberfläche enthält. Weitere Informationen finden Sie unter [Binärtyp](binary-type.md).                  |
| Key    | Binary    | Symbol             | Fremdschlüssel zu einer Binärtabellenzeile, die ein Symbol für die Verwendung in der Benutzeroberfläche enthält. Weitere Informationen finden Sie unter [Binärtyp](binary-type.md).                   |
| Key    | Binary    | EXE              | Fremdschlüssel zu einer Binärtabellenzeile, die eine 32-Bit-EXE-Datei enthält. Weitere Informationen finden Sie unter [Binärtyp](binary-type.md).                             |
| Key    | Binary    | EXE64            | Fremdschlüssel für eine Binärtabellenzeile, die eine 32- oder 64-Bit-EXE enthält. Weitere Informationen finden Sie unter [Binärtyp](binary-type.md).                       |
| Key    | Symbol      | ShortcutIcon     | Fremdschlüssel für eine Symboltabellenzeile, die ein Symbol für die Verwendung durch eine Verknüpfung enthält. Weitere Informationen finden Sie unter [Symboltyp.](icon-type.md)                |
| Key    | Dialog    | DialogWeiter       | Fremdschlüssel für eine Dialogtabellenzeile. Weitere Informationen finden Sie [unter Dialogtyp.](dialog-type.md)                                                 |
| Key    | Dialog    | DialogPrev       | Fremdschlüssel für eine Dialogtabellenzeile. Weitere Informationen finden Sie [unter Dialogtyp.](dialog-type.md)                                                 |
| Key    | Verzeichnis | IsolationDir     | Fremdschlüssel zu einer Verzeichnistabellenzeile, zu der isolierte Dateien gehören. Weitere Informationen finden Sie unter [Verzeichnistyp](directory-type.md).            |
| Key    | Verzeichnis | ShortcutLocation | Fremdschlüssel zu einer Verzeichnistabellenzeile, in der eine Verknüpfung installiert werden soll. Weitere Informationen finden Sie unter [Verzeichnistyp](directory-type.md).   |
| Key    | Eigenschaft  |                  | Fremdschlüssel für eine Eigenschaftenzeile. Weitere Informationen finden Sie unter [Eigenschaftentyp.](property-type.md)                                                 |
| Key    | Eigenschaft  | Öffentlich           | Fremdschlüssel für eine Eigenschaftenzeile. Weitere Informationen finden Sie unter [Eigenschaftentyp.](property-type.md)                                                 |
| Key    | Eigenschaft  | Privat          | Fremdschlüssel zu einer Eigenschaftenzeile. Weitere Informationen [finden Sie unter Eigenschaftentyp](property-type.md).                                                 |



 

[Bitfield-Formattypen](bitfield-format-types.md)



| Format   | type | ContextData                                  | BESCHREIBUNG                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bitfield |      | <mask>;<A>=<a>;<B> =b | Ändert eine Teilmenge von Bits in einer Spalte. Weitere Informationen [finden Sie unter Beliebiger Bitfeldtyp.](arbitrary-bitfield-type.md) |



 

 

 



