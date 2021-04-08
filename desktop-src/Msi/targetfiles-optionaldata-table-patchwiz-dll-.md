---
description: Die Tabelle "targetfiles \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem Zielimage. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der uikreatepatchpackageex-Funktion verwendet.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960148"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>Targetfiles \_ (OptionalData-Tabelle) (Patchwiz.dll)

Die Tabelle "targetfiles \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem Zielimage. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die Tabelle "targetfiles \_ OptionalData" enthält die folgenden Spalten.



| Spalte        | Typ | Schlüssel | Nullwerte zulässig |
|---------------|------|-----|----------|
| Ziel        | text | J   | N        |
| FTK           | text | J   | N        |
| SymbolPath   | text |     | J        |
| Ignoreoffsets | text |     | J        |
| Ignorelengths | text |     | J        |
| Retainoffsets | text |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar
</dt> <dd>

Fremdschlüssel für die Ziel Spalte der [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in die [Dateitabelle](file-table.md) des zielbilds.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath
</dt> <dd>

Der Wert in diesem Feld wird der durch Semikolons getrennten Liste der Ordner in der SymbolPath-Spalte der [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann zum Hinzufügen von Symbol Dateien für eine bestimmte Datei verwendet werden.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>Ignoreoffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der Zieldatei ignoriert werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte ignorelengths identisch sein. Diese Spalte ist optional.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>Ignorelengths
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Längen in Bytes für die Bereiche, die in der Zieldatei ignoriert werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der ignoreoffsets-Spalte identisch sein. Diese Spalte ist optional.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets
</dt> <dd>

Der Wert in diesem Feld ist eine durch Trennzeichen getrennte Liste von Bereichs Offset Zahlen für die Bereiche, die in der Zieldatei beibehalten werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainoffsets" des entsprechenden Datensatzes in der [Tabelle "familyfileranges" (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md) übereinstimmen.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



