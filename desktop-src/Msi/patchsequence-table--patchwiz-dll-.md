---
description: Die PatchSequence-Tabelle wird verwendet, um die MsiPatchSequence-Tabelle in einem Patch zu generieren. Die Tabelle erfordert die Version von PATCHWIZ.DLL, die mit Windows Installer&\# 160;3.0 verfügbar ist.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: PatchSequence-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0281f9882a674b268466259c534eefaa468bacf0fa891dc3a385e4d580a1e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129180"
---
# <a name="patchsequence-table-patchwizdll"></a>PatchSequence-Tabelle (PATCHWIZ.DLL)

Die PatchSequence-Tabelle wird verwendet, um die [MsiPatchSequence-Tabelle](msipatchsequence-table.md) in einem Patch zu generieren. Für die Tabelle ist die Version von [PATCHWIZ.DLL](patchwiz-dll.md) erforderlich, die mit Windows Installer 3.0 verfügbar ist.

In der folgenden Tabelle sind die Spalten der PatchSequence-Tabelle aufgeführt.



| Spalte      | Typ       | Key | Nullwerte zulässig |
|-------------|------------|-----|----------|
| PatchFamily | Bezeichner | J   | N        |
| Ziel      | Text       | J   | J        |
| Sequenz    | Version    |     | J        |
| Ersetzen   | Integer    |     | J        |



 

### <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Der Bezeichner, der die Sequenzfamilien angibt, zu denen dieser Patch gehört.

Die Werte in den Spalten Target und PatchFamily definieren zusammen den Primärschlüssel für die Tabelle. Ein Patch, der zu mehreren Sequenzfamilien gehört oder je nach Produktcode des Ziels über unterschiedliche Sequenzen verfügt, kann für jede Kopplung eine Zeile enthalten. Dieser Wert wird verwendet, um die PatchFamily-Spalte der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) zu füllen, die zum Patch gehört.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Ziel
</dt> <dd>

Die Spalte Ziel wird verwendet, um patchFamily nach Produktcode zu filtern.

Ein NULL-Wert in dieser Spalte gibt an, dass diese PatchFamily für alle Ziele des Patches gilt. Wenn diese Spalte einen Fremdschlüssel für die [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)enthält, wird der Produktcode des angegebenen Bilds abgerufen und zum Auffüllen des Produktcodewerts in der Zeile des neuen Patches der [MsiPatchSequence-Tabelle verwendet.](msipatchsequence-table.md) Wenn diese Spalte eine GUID enthält, wird die GUID verwendet, um den Produktcodewert der Zeile in der MsiPatchSequence-Tabelle zu füllen.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Der Wert in der Spalte Sequenz wird verwendet, um die Sequence -Spalte der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) der neuen Patchdatei zu füllen.

Wenn der Wert NULL ist, wird automatisch eine Sequenznummer generiert.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Ersetzen
</dt> <dd>

Der Wert **msidbPatchSequenceSupersedeEarlier** oder 1 in diesem Feld gibt an, dass dieser Patch frühere kleine Updates [in](small-updates.md) den Sequenzfamilien absetzt, zu denen dieser Patch gehört.

Der Wert in dieser Spalte wird verwendet, um die Attributes -Spalte der Zeile des neuen Patches in der [MsiPatchSequence-Tabelle fest.](msipatchsequence-table.md)

</dd> </dl>

### <a name="remarks"></a>Hinweise

Verfügbar ab Windows Installer 3.0.

 

 



