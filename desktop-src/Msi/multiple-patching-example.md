---
description: Das folgende Beispiel zeigt, wie Windows Installer 3.0 und höher verwendet werden kann, um Patches in der Reihenfolge anzuwenden, in der sie erstellt werden.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Beispiel für mehrere Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8d33d103bb27fde3b7fdc4ee46a0c5d946e73b6948513ea1b8fffb7bab30bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943367"
---
# <a name="multiple-patching-example"></a>Beispiel für mehrere Patches

Das folgende Beispiel zeigt, wie Windows Installer 3.0 und höher verwendet werden kann, um Patches in der Reihenfolge anzuwenden, in der sie erstellt werden.

## <a name="example"></a>Beispiel

In diesem Beispiel gibt es drei Patches: QFE1, QFE2 und ServicePack1, und sie verfügen jeweils über eine [MsiPatchSequence-Tabelle.](msipatchsequence-table.md) Diese Patches wurden so erstellt, dass sie auf Version 1.0 der Anwendung angewendet werden.



| Patchname   | Patchtyp    | Sequenznummer |
|--------------|---------------|-----------------|
| QFE1         | Kleines Update  | 1.1.0           |
| QFE2         | Kleines Update  | 1.2.0           |
| ServicePack1 | Kleineres Upgrade | 1.3.0           |



 

Die [MsiPatchSequence-Tabelle](msipatchsequence-table.md) jedes Patches enthält nur einen Datensatz, der die Patchfamilie, den Produktcode und die Sequenznummer enthält. Die drei Patches werden alle auf dasselbe Produkt angewendet und gehören zur gleichen Patchfamilie namens AppPatch. Keiner der Patches weist das **msidbPatchSequenceSupersedeEarlier-Attribut** auf.

[MsiPatchSequence-Tabelle](msipatchsequence-table.md) für das [kleine QFE1-Update.](small-updates.md) 

| PatchFamily | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[MsiPatchSequence-Tabelle](msipatchsequence-table.md) für das [kleine QFE2-Update.](small-updates.md) 

| PatchFamily | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[MsiPatchSequence-Tabelle](msipatchsequence-table.md) für [ServicePack1-Nebenupgrade.](minor-upgrades.md) 

| PatchFamily | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Wenn ein Benutzer Version 1.0 des Produkts installiert und dann QFE2 anwendet und dann zu einem späteren Zeitpunkt entscheidet, QFE1 anzuwenden, stellt Windows Installer sicher, dass die effektive Sequenz der Patchanwendung auf das Produkt QFE1 vor QFE2 angewendet wird. Wenn der Benutzer ServicePack1 anwendet, wendet QFE2 und QFE1 zu einem späteren Zeitpunkt zusammen an, Windows Installer stellt sicher, dass die effektive Sequenz der Patchanwendung für das Produkt QFE1 vor QFE2 und vor ServicePack1 ist.

Wenn für ServicePack1 **msidbPatchSequenceSupersedeEarlier** in der Spalte Attributes der [Tabelle MsiPatchSequence](msipatchsequence-table.md) festgelegt ist, bedeutet dies, dass das Service Pack alle Änderungen in QFE1 und QFE2 enthält. In diesem Fall werden QFE1 und QFE2 nicht angewendet, wenn ServicePack1 angewendet wird.

**Windows Installer 2.0:** Wird nicht unterstützt. Versionen vor Windows Installer 3.0 können nur einen Patch pro Transaktion installieren, und Patches werden in der reihenfolge angewendet, in der sie bereitgestellt werden. Wenn im vorherigen Beispiel zuerst QFE2 und dann QFE1 angewendet wird, sind dies zwei Transaktionen, und die Patches werden auf Version 1.0 der Anwendung in der Sequenz QFE2 gefolgt von QFE1 angewendet. Wenn ServicePack1 zuerst angewendet wird, kann QFE1 oder QFE2 in einer späteren Transaktion nicht angewendet werden, da ServicePack1 ein kleineres Upgrade ist, das die Anwendungsversion ändert. QFE1 und QFE2 können nur auf Version 1.0 der Anwendung angewendet werden.

 

 



