---
description: Die Tabelle ExternalFiles enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären Zielimages sind.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: ExternalFiles-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2573556e8e4e00cf9004b83520468724ad1c959704cf8be32769a7ee41e24ebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636877"
---
# <a name="externalfiles-table-patchwizdll"></a>ExternalFiles-Tabelle (Patchwiz.dll)

Die Tabelle ExternalFiles enthält Informationen zu bestimmten Dateien, die nicht Teil eines regulären Zielimages sind. Diese Dateien können in Produkten vorhanden sein, die von einem anderen Produkt, Upgrade oder Patch aktualisiert wurden. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) verwendet.

Die ExternalFiles-Tabelle enthält die folgenden Spalten.



| Spalte        | Typ    | Key | Nullwerte zulässig |
|---------------|---------|-----|----------|
| Familie        | text    | J   | N        |
| FTK           | text    | J   | N        |
| FilePath      | text    | J   | N        |
| SymbolPaths   | text    |     | J        |
| IgnoreOffsets | text    |     | J        |
| IgnoreLengths | text    |     | J        |
| RetainOffsets | text    |     | N        |
| Auftrag         | integer |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familie
</dt> <dd>

Fremdschlüssel für die Family -Spalte der [ImageFamilies-Tabelle (Patchwiz.dll).](imagefamilies-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in [Der Dateitabelle des](file-table.md) .msi datei des aktualisierten Images.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Filepath
</dt> <dd>

Vollständiger Pfad der externen Datei, einschließlich des Dateinamens. Das FilePath-Feld wird verwendet, um die in der FTK-Spalte angegebene Datei zu suchen.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Vollständiger Pfad, der nach Symboldateien der datei gesucht wurde, die in der FTK-Spalte angegeben ist.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichsoffsetnummern für die Bereiche, die in der externen Datei ignoriert werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der IgnoreLengths-Spalte übereinstimmen. Diese Spalte ist optional.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichslängen in Bytes für die Bereiche, die in der externen Datei ignoriert werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der IgnoreOffsets-Spalte übereinstimmen. Diese Spalte ist optional.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichsoffsetnummern für die Bereiche, die in der externen Datei beibehalten werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der RetainOffsets -Spalte des entsprechenden Datensatzes in der [FamilyFileRanges-Tabelle (Patchwiz.dll) übereinstimmen.](familyfileranges-table-patchwiz-dll-.md)

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Wenn mindestens zwei Versionen für dieselbe externe Datei angegeben werden, enthält die Tabelle möglicherweise mehrere Datensätze mit übereinstimmenden Werten in den Feldern FTK und Family. In diesem Fall kann das Feld Reihenfolge die Reihenfolge der externen Dateien angeben, die beim Erstellen des Patches verwendet werden. Die Reihenfolge liegt zwischen der ältesten und der neuesten Version.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle akzeptiert Umgebungsvariablen als Pfade ab Version 4.0 Patchwiz.dll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



