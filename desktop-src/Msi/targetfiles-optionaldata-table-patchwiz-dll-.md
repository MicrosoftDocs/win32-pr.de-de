---
description: Die Tabelle TargetFiles \_ OptionalData enthält Informationen zu bestimmten Dateien in einem Zielimage. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der UiCreatePatchPackageEx-Funktion verwendet.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5664e2e21968cb3fee5ce3d606dd07008f2436c4b649a7bcefeebd77df9cf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623735"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>TargetFiles \_ OptionalData Table (Patchwiz.dll)

Die Tabelle TargetFiles \_ OptionalData enthält Informationen zu bestimmten Dateien in einem Zielimage. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) verwendet.

Die Tabelle TargetFiles \_ OptionalData enthält die folgenden Spalten.



| Spalte        | Typ | Key | Nullwerte zulässig |
|---------------|------|-----|----------|
| Ziel        | text | J   | N        |
| FTK           | text | J   | N        |
| SymbolPaths   | text |     | J        |
| IgnoreOffsets | text |     | J        |
| IgnoreLengths | text |     | J        |
| RetainOffsets | text |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Ziel
</dt> <dd>

Fremdschlüssel für die Target -Spalte der [TargetImages-Tabelle (Patchwiz.dll).](targetimages-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in der [Dateitabelle des](file-table.md) Zielbilds.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Der Wert in diesem Feld wird der durch Semikolons getrennten Liste von Ordnern in der SymbolPaths -Spalte der [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann verwendet werden, um Symboldateien für eine bestimmte Datei hinzuzufügen.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichsoffsetnummern für die Bereiche, die in der Zieldatei ignoriert werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der IgnoreLengths-Spalte übereinstimmen. Diese Spalte ist optional.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichslängen in Bytes für die Bereiche, die in der Zieldatei ignoriert werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der IgnoreOffsets-Spalte übereinstimmen. Diese Spalte ist optional.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichsoffsetnummern für die Bereiche, die in der Zieldatei beibehalten werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste müssen mit den Elementen in der RetainOffsets-Spalte des entsprechenden Datensatzes in der [FamilyFileRanges-Tabelle (Patchwiz.dll) übereinstimmen.](familyfileranges-table-patchwiz-dll-.md)

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, Patchwiz.dll werden die Werte in ULONGs konvertiert.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



