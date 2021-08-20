---
description: Die Signaturtabelle enthält die Informationen, die eine Dateisignatur eindeutig identifizieren. Weitere Informationen zu Signaturen finden Sie unter Digitale Signaturen und Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Signaturtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ddda5c501b24e12498f356c10a1aa2a3549426daca5e4cc3c19c1f62ed04cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624647"
---
# <a name="signature-table"></a>Signaturtabelle

Die Signaturtabelle enthält die Informationen, die eine Dateisignatur eindeutig identifizieren. Weitere Informationen zu Signaturen finden Sie unter [Digitale Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md)

Die Signaturtabelle enthält die folgenden Spalten.



| Spalte     | Typ                               | Key | Nullwerte zulässig |
|------------|------------------------------------|-----|----------|
| Signatur  | [Identifier](identifier.md)       | J   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| Minversion | [Text](text.md)                   | N   | J        |
| MaxVersion | [Text](text.md)                   | N   | J        |
| Minsize    | [DoubleInteger](doubleinteger.md) | N   | J        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | J        |
| Mindate    | [DoubleInteger](doubleinteger.md) | N   | J        |
| Maxdate    | [DoubleInteger](doubleinteger.md) | N   | J        |
| Languages  | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatur
</dt> <dd>

Die Spalte Signatur ist eine eindeutige Dateisignatur.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Der Name der Datei.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>Minversion
</dt> <dd>

Die Mindestversion der Datei mit einem Sprachvergleich. Wenn dieses Feld angegeben ist, muss die Datei über eine Version verfügen, die mindestens minVersion entspricht. Wenn die Datei eine gleiche Version wie der MinVersion-Feldwert aufweist, sich die in der Spalte Sprachen angegebene Sprache jedoch unterscheidet, erfüllt die Datei nicht die Signaturfilterkriterien.

> [!Note]  
> Die in der Spalte Sprachen angegebene Sprache wird im Vergleich verwendet, und es gibt keine Möglichkeit, sprache zu ignorieren. Wenn eine Datei die MinVersion-Feldanforderung unabhängig von der Sprache erfüllen soll, müssen Sie im Feld MinVersion einen Wert eingeben, der kleiner als der tatsächliche Wert ist. Wenn die Mindestversion für den Filter beispielsweise 2.0.2600.1183 ist, verwenden Sie 2.0.2600.1182, um die Datei ohne Übereinstimmung mit den Sprachinformationen zu suchen.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Die maximale Version der Datei. Wenn dieses Feld angegeben wird, muss die Datei über eine Version verfügen, die maximal gleich MaxVersion ist.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>Minsize
</dt> <dd>

Die Mindestgröße der Datei. Wenn dieses Feld angegeben ist, muss die untersuchte Datei mindestens eine Größe aufweisen, die MinSize entspricht. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Maxsize
</dt> <dd>

Die maximale Größe der Datei. Wenn dieses Feld angegeben ist, muss die Datei, die untersucht wird, eine Größe aufweisen, die maximal maxSize entspricht. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>Mindate
</dt> <dd>

Das Minimale Änderungsdatum und die Minimale Änderungszeit der Datei. Wenn dieses Feld angegeben ist, muss die untersuchte Datei ein Änderungsdatum und eine Änderungszeit aufweisen, die mindestens minDate entspricht. Dies muss eine nicht negative Zahl sein. Das Format dieses Felds ist zwei gepackte 16-Bit-Werte vom Typ **WORD**. Der **WORD-Wert** mit hoher Reihenfolge gibt das Datum im MS-DOS-Datumsformat an. Der **WORD-Wert** mit niedriger Reihenfolge gibt die Zeit im MS-DOS-Zeitformat an. Der Wert 0 für den Zeitwert stellt Mitternacht dar. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>Maxdate
</dt> <dd>

Das maximale Erstellungsdatum der Datei. Wenn dieses Feld angegeben ist, muss die Datei, die überprüft wird, über ein Erstellungsdatum verfügen, das maximal maxDate entspricht. Dies muss eine nicht negative Zahl sein. Das Format dieses Felds ist zwei gepackte 16-Bit-Werte vom Typ **WORD**. Der **WORD-Wert** mit hoher Reihenfolge gibt das Datum im MS-DOS-Datumsformat an. Der **WORD-Wert** mit niedriger Reihenfolge gibt die Zeit im MS-DOS-Zeitformat an. Der Wert 0 für den Zeitwert stellt Mitternacht dar. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Sprachen
</dt> <dd>

Die von der Datei unterstützten Sprachen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Signatur wird mithilfe der [RegLocator-Tabelle,](reglocator-table.md)der [IniLocator-Tabelle,](inilocator-table.md)der [CompLocator-Tabelle](complocator-table.md)und der [DrLocator-Tabelle](drlocator-table.md)durchsucht. Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor entscheidet, nach Produkten in mehreren Sprachen zu suchen, kann die Tabelle für jede Sprache einen separaten Eintrag enthalten.

Die Signaturtabelle folgt im Allgemeinen den Windows Regeln für die [Dateiversionsversionierung](file-versioning-rules.md)des Installationsprogramms. Die in der Spalte Sprachen der Signaturtabelle angegebenen Sprachen werden nur ausgewertet, wenn die Dateiversionen gleichwertig sind. Die Spalte Sprachen stellt sicher, dass eine Datei einer bestimmten Sprache entspricht, wenn sie der angeforderten Version entspricht. Es ist keine Methode verfügbar, um die Spalte Languages zu ignorieren. Ein NULL-Wert, der in die Spalte Languages eingegeben wird, wird als Datei ohne Sprache behandelt und stimmt nicht mit der Dateisignatur einer Datei mit einer Sprache überein, die in der Signaturtabelle angezeigt wird. Im folgenden Beispiel wird nach einer bestimmten Version von MSI.DLL.

[DrLocator-Tabelle](drlocator-table.md)

| Signatur\_ | Parent | Pfad                  | Tiefe |
|-------------|--------|-----------------------|-------|
| MsiDll      | {null} | c: \\ windows \\ system32 | 0     |



 

[AppSearch-Tabelle](appsearch-table.md)



| Eigenschaft | Signatur\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Signaturtabelle



| Signatur | FileName | Minversion    | MaxVersion | Minsize | MaxSize | Mindate | Maxdate | Languages |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | {null}     | {null}  | {null}  | {null}  | {null}  | 0         |



 

In diesem Fall und auf Windows XP SP1 legt die [AppSearch-Aktion](appsearch-action.md) MSIDLL auf c: windows system32msi.dll fest, da MSI.DLL eine sprachneutrale Datei \\ \\ \\ ist. Wenn der Wert der Spalte Languages von 0 in 1033 geändert wird, kann die AppSearch-Aktion die übereinstimmende msi.dll nicht finden, und die MSIDLL-Eigenschaft ist nicht definiert.

Sie können die Signaturtabelle nicht verwenden, um Abfragen für Sprachen allein auszuführen. Um nach verschiedenen Sprachversionen einer Datei zu suchen, müssen Sie für jede Sprachversion über einen separaten Eintrag in der Signaturtabelle verfügen. Wenn in der Spalte Sprachen mehrere Sprachen angegeben sind, wird nach einer Datei gesucht, die alle diese Sprachen unterstützt.

Das Format der Spalten MinDate und MaxDate sind zwei gepackte 16-Bit-Werte vom **Typ WORD**.

**Word-Datum**



| Bits | Content                                             |
|------|-----------------------------------------------------|
| 0–4  | Tag des Monats (1-31)                             |
| 5-8  | Monat (1 = Januar, 2 = Februar, und so weiter)        |
| 9-15 | Jahresoffset von 1980 (addieren Sie 1980, um das tatsächliche Jahr zu erhalten) |



 

**Word-Zeit**



| Bits  | Content                     |
|-------|-----------------------------|
| 0–4   | Sekunden geteilt durch 2        |
| 5-10  | Minuten (0-59)              |
| 11-15 | Hour(0-23 on 24 hour clock) |



 

Die Formel zum Berechnen der MinDate- und MaxDate-Feldwerte ist:

( (Jahr - 1980) \* 512 + Monat \* 32 + Tag ) \* 65536 + Stunden \* 2048 + Minuten \* 32 + Sekunden/2

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



