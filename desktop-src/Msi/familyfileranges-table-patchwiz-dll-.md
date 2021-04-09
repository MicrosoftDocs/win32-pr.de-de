---
description: Die familyfileranges-Tabelle enthält Informationen zu bestimmten Dateien eines aktualisierten Bilds mit Bereichen, die nie überschrieben werden sollten.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Familyfileranges-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130677"
---
# <a name="familyfileranges-table-patchwizdll"></a>Familyfileranges-Tabelle (Patchwiz.dll)

Die familyfileranges-Tabelle enthält Informationen zu bestimmten Dateien eines aktualisierten Bilds mit Bereichen, die nie überschrieben werden sollten. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die familyfileranges-Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ | Schlüssel | Nullwerte zulässig |
|---------------|------|-----|----------|
| Familie        | text | J   | N        |
| FTK           | text | J   | N        |
| Retainoffsets | text |     | N        |
| Retainlängen | text |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte
</dt> <dd>

Fremdschlüssel für die Spalte "Family" der [Tabelle "ImageFamilies" (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in den [Datei Tabellen](file-table.md) aller aktualisierten Images in der Abbild Familie.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>Retainoffsets
</dt> <dd>

Der Offset der Bereiche, die nicht überschrieben werden können. Der Wert in diesem Feld ist eine Liste der Bereichs Offset Zahlen für Bereiche, die in den Zieldateien nicht überschrieben werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der Spalte "retainlängen" identisch sein.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>Retainlängen
</dt> <dd>

Die Länge in Bytes der Bereiche, die nicht überschrieben werden können. Der Wert in diesem Feld ist eine Liste der Bereichs Längen Zahlen für Bereiche, die in Zieldateien beibehalten werden sollen. Die Reihenfolge und die Anzahl der Bereiche in der Liste müssen mit den Elementen in der retainoffsets-Spalte identisch sein.

Die Werte können Decimal oder hexadezimal sein. [Patchwiz.dll](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, und Patchwiz.dll konvertiert die Werte in ulongs.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die in retainoffsets und retainlängen eingegebenen Offsets und Längen dürfen keine überlappenden Bereiche angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



