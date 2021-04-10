---
description: Die Tabelle "patchsequence" wird verwendet, um die msipatchsequence-Tabelle in einem Patch zu generieren. Die Tabelle erfordert die Version von PATCHWIZ.DLL, die mit Windows Installer&\# 160; 3.0 verfügbar ist.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Patchsequence-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868847"
---
# <a name="patchsequence-table-patchwizdll"></a>Patchsequence-Tabelle (PATCHWIZ.DLL)

Die Tabelle "patchsequence" wird verwendet, um die [msipatchsequence-Tabelle](msipatchsequence-table.md) in einem Patch zu generieren. Die Tabelle erfordert die Version von [PATCHWIZ.DLL](patchwiz-dll.md) , die in Windows Installer 3,0 verfügbar ist.

In der folgenden Tabelle sind die Spalten der Tabelle patchsequence aufgeführt.



| Spalte      | Typ       | Schlüssel | Nullwerte zulässig |
|-------------|------------|-----|----------|
| Patchfamilie | Bezeichner | J   | N        |
| Ziel      | Text       | J   | J        |
| Sequenz    | Version    |     | J        |
| Ablösen   | Integer    |     | J        |



 

### <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>Patchfamilie
</dt> <dd>

Der Bezeichner, der die Sequenz Familien angibt, zu denen dieser Patch gehört.

Die Werte in den Spalten Ziel und patchfamilie definieren den Primärschlüssel für die Tabelle. Ein Patch, der zu mehreren Sequenz Familien gehört oder je nach Produktcode über unterschiedliche Sequenzen verfügt, kann für jede Kopplung eine Zeile aufweisen. Dieser Wert wird verwendet, um die patchfamily-Spalte der [msipatchsequence-Tabelle](msipatchsequence-table.md) aufzufüllen, die zum Patch gehört.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar
</dt> <dd>

Die Ziel Spalte wird verwendet, um die patchfamilie nach Produktcode zu filtern.

Ein NULL-Wert in dieser Spalte gibt an, dass diese patchfamilie für alle Ziele des Patches gilt. Wenn diese Spalte einen Fremdschlüssel für die [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)enthält, wird der Produktcode des angegebenen Bilds abgerufen und verwendet, um den Product Code-Wert in der Zeile des neuen Patches der [msipatchsequence-Tabelle](msipatchsequence-table.md)aufzufüllen. Wenn diese Spalte eine GUID enthält, wird die GUID verwendet, um den Product Code-Wert der Zeile in der msipatchsequence-Tabelle aufzufüllen.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Der Wert in der Sequenz Spalte wird verwendet, um die Sequence-Spalte der [msipatchsequence-Tabelle](msipatchsequence-table.md) der neuen Patchdatei aufzufüllen.

Wenn der Wert NULL ist, wird automatisch eine Sequenznummer generiert.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Ablösen
</dt> <dd>

Der Wert **msidbpatchsequencesupersedefrühere** oder 1 in diesem Feld gibt an, dass dieser Patch frühere [kleine Updates](small-updates.md) in den Sequenz Familien ersetzt, zu denen dieser Patch gehört.

Der Wert in dieser Spalte wird verwendet, um die Spalte Attribute der Zeile des neuen Patches in der [msipatchsequence-Tabelle](msipatchsequence-table.md) festzulegen.

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Verfügbar ab Windows Installer 3,0.

 

 



