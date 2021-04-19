---
description: Die Signatur Tabelle enthält die Informationen, die eine Datei Signatur eindeutig identifizieren. Weitere Informationen zu Signaturen finden Sie unter digitale Signaturen und Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Signatur Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348702"
---
# <a name="signature-table"></a>Signatur Tabelle

Die Signatur Tabelle enthält die Informationen, die eine Datei Signatur eindeutig identifizieren. Weitere Informationen zu Signaturen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).

Die Signatur Tabelle weist die folgenden Spalten auf.



| Spalte     | Typ                               | Schlüssel | Nullwerte zulässig |
|------------|------------------------------------|-----|----------|
| Signatur  | [Bezeichner](identifier.md)       | J   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | J        |
| MaxVersion | [Text](text.md)                   | N   | J        |
| MinSize    | [Doubleiteger](doubleinteger.md) | N   | J        |
| MaxSize    | [Doubleiteger](doubleinteger.md) | N   | J        |
| MinDate    | [Doubleiteger](doubleinteger.md) | N   | J        |
| MaxDate    | [Doubleiteger](doubleinteger.md) | N   | J        |
| Sprachen  | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Unter
</dt> <dd>

Die Signatur Spalte ist eine eindeutige Datei Signatur.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der Name der Datei.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

Die minimale Version der Datei mit einem sprach Vergleich. Wenn dieses Feld angegeben wird, muss die Datei eine Version aufweisen, die mindestens mit MinVersion identisch ist. Wenn die Datei eine gleiche Version wie der Wert für das MinVersion-Feld aufweist, die in der Spalte Sprachen angegebene Sprache jedoch unterschiedlich ist, erfüllt die Datei die Signatur Filterkriterien nicht.

> [!Note]  
> Die in der Spalte Sprachen angegebene Sprache wird im Vergleich verwendet, und es gibt keine Möglichkeit, die Sprache zu ignorieren. Wenn eine Datei die MinVersion-Feld Anforderung unabhängig von der Sprache erfüllen soll, müssen Sie einen Wert im MinVersion-Feld eingeben, der einen Wert kleiner als der tatsächliche Wert ist. Wenn die Mindestversion für den Filter beispielsweise 2.0.2600.1183 ist, verwenden Sie 2.0.2600.1182, um die Datei zu suchen, ohne die Sprachinformationen zu entsprechen.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Die maximale Version der Datei. Wenn dieses Feld angegeben wird, muss die Datei eine Version aufweisen, die höchstens MaxVersion entspricht.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Die minimale Größe der Datei. Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei eine Größe aufweisen, die mindestens MinSize entspricht. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize
</dt> <dd>

Die maximale Größe der Datei. Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei eine Größe aufweisen, die höchstens MaxSize entspricht. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

Der minimale Änderungs Zeitpunkt (Datum und Uhrzeit) der Datei. Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei ein Änderungsdatum und eine Uhrzeit aufweisen, die mindestens MinDate entsprechen. Dabei muss es sich um eine nicht negative Zahl handeln. Das Format dieses Felds besteht aus zwei packenden 16-Bit-Werten vom Typ **Word**. Der Wert für das hohe Bestell **Wort** gibt das Datum im MS-DOS-Datumsformat an. Der **Word** -Wert mit niedriger Ordnung gibt die Zeit im MS-DOS-Zeitformat an. Der Wert 0 für den Uhrzeitwert ist Mitternacht. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

Das maximale Erstellungsdatum der Datei. Wenn dieses Feld angegeben ist, muss die zu überprüfende Datei ein Erstellungsdatum aufweisen, das höchstens MaxDate entspricht. Dabei muss es sich um eine nicht negative Zahl handeln. Das Format dieses Felds besteht aus zwei packenden 16-Bit-Werten vom Typ **Word**. Der Wert für das hohe Bestell **Wort** gibt das Datum im MS-DOS-Datumsformat an. Der **Word** -Wert mit niedriger Ordnung gibt die Zeit im MS-DOS-Zeitformat an. Der Wert 0 für den Uhrzeitwert ist Mitternacht. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Sprachen
</dt> <dd>

Die von der Datei unterstützten Sprachen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Signatur wird mithilfe der [reglocator-Tabelle](reglocator-table.md), der [inilocator](inilocator-table.md)-Tabelle, der [complocator](complocator-table.md)-Tabelle und der [drlocator-Tabelle](drlocator-table.md)durchsucht. Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.

Die Signatur Tabelle folgt in der Regel den Windows Installer [Datei Versions Regeln](file-versioning-rules.md). Die in der Spalte Sprachen der Signatur Tabelle angegebenen Sprachen werden nur ausgewertet, wenn die Dateiversionen äquivalent sind. In der Spalte Sprachen wird sichergestellt, dass eine Datei eine bestimmte Sprache hat, wenn Sie die angeforderte Version hat. Es ist keine Methode zum Ignorieren der Spalte Sprachen verfügbar. Ein in die Spalte Sprachen eingegebener NULL-Wert wird als Datei ohne Sprache behandelt und entspricht nicht der Datei Signatur einer Datei, die in der Signatur Tabelle enthalten ist. Im folgenden Beispiel wird nach einer bestimmten Version von MSI.DLL gesucht.

[Drlocator-Tabelle](drlocator-table.md)

| Signatur\_ | Parent | Pfad                  | Tiefe |
|-------------|--------|-----------------------|-------|
| MsiDll      | normal | c: \\ Windows \\ system32 | 0     |



 

[AppSearch-Tabelle](appsearch-table.md)



| Eigenschaft | Signatur\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Signatur Tabelle



| Signatur | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | MinDate | MaxDate | Sprachen |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | normal     | normal  | normal  | normal  | normal  | 0         |



 

In diesem Fall und unter Windows XP SP1 legt die [AppSearch-Aktion](appsearch-action.md) msidll auf c: \\ Windows System32msi.dll fest, \\ \\ da MSI.DLL eine sprachneutrale Datei ist. Wenn der Wert der Sprachen-Spalte von 0 in 1033 geändert wird, kann die AppSearch-Aktion die übereinstimmende msi.dll nicht finden, und die msidll-Eigenschaft ist nicht definiert.

Sie können die Signatur Tabelle nicht zum Abfragen von Sprachen allein verwenden. Um nach verschiedenen Sprachversionen einer Datei zu suchen, benötigen Sie einen separaten Eintrag in der Signatur Tabelle für jede Sprachversion. Wenn in der Spalte Sprachen mehrere Sprachen bereitgestellt werden, ist die Suche nach einer Datei, die alle diese Sprachen unterstützt.

Das Format der Spalten MinDate und MaxDate sind zwei gepackte 16-Bit-Werte vom Typ **Word**.

Datums **Wort**



| Bits | Inhalt                                             |
|------|-----------------------------------------------------|
| 0 – 4  | Tag des Monats (1-31)                             |
| 5-8  | Monat (1 = Januar, 2 = Februar usw.)        |
| 9-15 | Jahr Offset von 1980 (Hinzufügen von 1980, um das tatsächliche Jahr zu erhalten) |



 

Zeit **Wort**



| Bits  | Inhalt                     |
|-------|-----------------------------|
| 0 – 4   | Sekunden geteilt durch 2        |
| 5-10  | Minuten (0-59)              |
| 11-15 | Stunde (0 bis 23 Uhr auf 24 Stunden) |



 

Die Formel zum Berechnen der Werte für MinDate und MaxDate ist:

((Jahr-1980) \* 512 + Monat \* 32 + Tag) \* 65536 + Stunden \* 2048 + Minuten \* 32 + Sekunden/2

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



