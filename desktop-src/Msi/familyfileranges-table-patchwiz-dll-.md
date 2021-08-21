---
description: Die Tabelle FamilyFileRanges enthält Informationen zu bestimmten Dateien eines aktualisierten Images mit Bereichen, die nie überschrieben werden sollten.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: FamilyFileRanges-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0559f4cea1061f9cf0c1438140e7abba8b00908233a1a1d608ae5dbd8b79ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636897"
---
# <a name="familyfileranges-table-patchwizdll"></a>FamilyFileRanges-Tabelle (Patchwiz.dll)

Die Tabelle FamilyFileRanges enthält Informationen zu bestimmten Dateien eines aktualisierten Images mit Bereichen, die nie überschrieben werden sollten. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) verwendet.

Die FamilyFileRanges-Tabelle enthält die folgenden Spalten.



| Spalte        | Typ | Key | Nullwerte zulässig |
|---------------|------|-----|----------|
| Familie        | text | J   | N        |
| FTK           | text | J   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familie
</dt> <dd>

Fremdschlüssel für die Spalte Family der [ImageFamilies-Tabelle (Patchwiz.dll).](imagefamilies-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in die [Dateitabellen](file-table.md) aller aktualisierten Images in der Imagefamilie.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

Der Offset der Bereiche, die nicht überschrieben werden können. Der Wert in diesem Feld ist eine Liste der Bereichsoffsetnummern für Bereiche, die in den Zieldateien nicht überschrieben werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste muss mit den Elementen in der RetainLengths-Spalte übereinstimmen.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, und Patchwiz.dll konvertiert die Werte in ULONGs.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

Die Länge der Bereiche in Bytes, die nicht überschrieben werden können. Der Wert in diesem Feld ist eine Liste von Bereichslängennummern für Bereiche, die in Zieldateien beibehalten werden sollen. Die Reihenfolge und Anzahl der Bereiche in der Liste muss mit den Elementen in der RetainOffsets -Spalte übereinstimmen.

Die Werte können dezimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn ihm "0x" vorangestellt ist. Die Spalten sind Zeichenfolgenspalten, und Patchwiz.dll konvertiert die Werte in ULONGs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die in RetainOffsets und RetainLengths eingegebenen Offsets und Längen dürfen keine überlappenden Bereiche angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



