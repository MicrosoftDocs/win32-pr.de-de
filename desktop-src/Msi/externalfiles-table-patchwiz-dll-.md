---
description: Die externalfiles-Tabelle enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären zielbilds sind.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Externalfiles-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528196"
---
# <a name="externalfiles-table-patchwizdll"></a>Externalfiles-Tabelle (Patchwiz.dll)

Die externalfiles-Tabelle enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären zielbilds sind. Diese Dateien können in Produkten vorhanden sein, die von einem anderen Produkt, Upgrade oder Patch aktualisiert wurden. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die externalfiles-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ    | Schlüssel | Nullwerte zulässig |
|---------------|---------|-----|----------|
| Familie        | text    | J   | N        |
| FTK           | text    | J   | N        |
| FilePath      | text    | J   | N        |
| SymbolPath   | text    |     | J        |
| Ignoreoffsets | text    |     | J        |
| Ignorelengths | text    |     | J        |
| Retainoffsets | text    |     | N        |
| Auftrag         | integer |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte
</dt> <dd>

Fremdschlüssel für die Spalte "Family" der [Tabelle "ImageFamilies" (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in die [Dateitabelle](file-table.md) der MSI-Datei des aktualisierten Abbilds.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath
</dt> <dd>

Vollständiger Pfad der externen Datei, einschließlich des Datei namens. Das Feld "filePath" wird verwendet, um die in der FTK-Spalte angegebene Datei zu suchen.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath
</dt> <dd>

Vollständiger Pfad für Symbol Dateien der Datei, die in der FTK-Spalte angegeben ist.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>Ignoreoffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der externen Datei ignoriert werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte ignorelengths identisch sein. Diese Spalte ist optional.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>Ignorelengths
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Längen in Bytes, die in der externen Datei ignoriert werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der ignoreoffsets-Spalte identisch sein. Diese Spalte ist optional.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der externen Datei aufbewahrt werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainoffsets" des entsprechenden Datensatzes in der [Tabelle "familyfileranges" (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)übereinstimmen.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Wenn für dieselbe externe Datei mindestens zwei Versionen angegeben sind, enthält die Tabelle möglicherweise mehrere Datensätze mit übereinstimmenden Werten in den Feldern FTK und Family. In diesem Fall kann das Feld Order die Reihenfolge externer Dateien angeben, die beim Erstellen des Patches verwendet werden soll. Die Reihenfolge ist von der ältesten zur neuesten Version.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle akzeptiert Umgebungsvariablen als Pfade, die mit Version 4,0 von Patchwiz.dll beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



