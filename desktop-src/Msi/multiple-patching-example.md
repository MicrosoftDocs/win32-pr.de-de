---
description: Das folgende Beispiel zeigt, wie Sie mit Windows Installer 3,0 und höher Patches in der Reihenfolge anwenden können, in der Sie erstellt wurden.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Beispiel für das mehrfache Patchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357498"
---
# <a name="multiple-patching-example"></a>Beispiel für das mehrfache Patchen

Das folgende Beispiel zeigt, wie Sie mit Windows Installer 3,0 und höher Patches in der Reihenfolge anwenden können, in der Sie erstellt wurden.

## <a name="example"></a>Beispiel

In diesem Beispiel gibt es drei Patches: QFE1, QFE2 und ServicePack1, und Sie verfügen jeweils über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle. Diese Patches wurden so verfasst, dass Sie auf Version 1,0 der Anwendung angewendet werden.



| Patchname   | Patchetyp    | Sequenznummer |
|--------------|---------------|-----------------|
| QFE1         | Kleines Update  | 1.1.0           |
| QFE2         | Kleines Update  | 1.2.0           |
| ServicePack1 | Geringfügige Aktualisierung | 1.3.0           |



 

Die [msipatchsequence](msipatchsequence-table.md) -Tabelle jedes Patches weist nur einen Datensatz auf, der die patchfamilie, den Produktcode und die Sequenznummer enthält. Die drei Patches werden alle auf das gleiche Produkt angewendet und gehören derselben patchfamilie mit dem Namen "AppPatch" an. Keines der Patches hat das **msidbpatchsequencesupersedebug** -Attribut.

[Msipatchsequence-Tabelle](msipatchsequence-table.md) für das QFE1 [Small Update](small-updates.md). 

| Patchfamilie | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18a9233c-0b34-4127-a966-c257386270bc} | 1.1.0    |            |



 

[Msipatchsequence-Tabelle](msipatchsequence-table.md) für das QFE2 [Small Update](small-updates.md). 

| Patchfamilie | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18a9233c-0b34-4127-a966-c257386270bc} | 1.2.0    |            |



 

[Msipatchsequence-Tabelle](msipatchsequence-table.md) für ServicePack1 [Minor Upgrade](minor-upgrades.md). 

| Patchfamilie | ProductCode                            | Sequenz | Attribute |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18a9233c-0b34-4127-a966-c257386270bc} | 1.3.0    |            |



 

Wenn ein Benutzerversion 1,0 des Produkts installiert und dann QFE2 anwendet und dann zu einem späteren Zeitpunkt QFE1 anwendet, stellt Windows Installer sicher, dass die effektive Sequenz der Patchanwendung für das Produkt QFE1 vor QFE2 angewendet wird. Wenn der Benutzer ServicePack1 anwendet, wendet QFE2 und QFE1 zu einem späteren Zeitpunkt an. Windows Installer stellt sicher, dass die effektive Sequenz der Patchanwendung für das Produkt QFE1 vor QFE2 und vor ServicePack1 liegt.

Wenn in ServicePack1 **msidbpatchsequencesupersedefrüher** in der Attribute-Spalte der [msipatchsequence](msipatchsequence-table.md) -Tabelle festgelegt ist, bedeutet dies, dass die Service Pack alle Änderungen in QFE1 und QFE2 enthält. In diesem Fall werden QFE1 und QFE2 nicht angewendet, wenn ServicePack1 angewendet wird.

**Windows Installer 2,0:** Nicht unterstützt. Frühere Versionen als Windows Installer 3,0 können nur einen Patch pro Transaktion installieren, und Patches werden in der Reihenfolge angewendet, in der Sie bereitgestellt werden. Wenn QFE2 im vorherigen Beispiel zuerst angewendet und dann QFE1 angewendet wird, werden zwei Transaktionen und die Patches auf Version 1,0 der Anwendung in der Sequenz QFE2 gefolgt von QFE1 angewendet. Wenn ServicePack1 zuerst angewendet wird, kann QFE1 oder QFE2 nicht in einer späteren Transaktion angewendet werden, da ServicePack1 ein kleineres Upgrade ist, bei dem die Anwendungs Version geändert wird. QFE1 und QFE2 können nur auf Version 1,0 der Anwendung angewendet werden.

 

 



