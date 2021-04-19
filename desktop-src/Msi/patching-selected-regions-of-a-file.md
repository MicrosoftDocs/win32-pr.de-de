---
description: Beim Patchen von Dateien mit variablen Inhalten ist es möglicherweise erforderlich, die ausgewählten Bereiche der Zieldatei beizubehalten, um den Verlust kritischer Informationen zu verhindern.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Patchen ausgewählter Bereiche einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778df4b0cc98eeacd1106929b18c7461c6fa9e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372908"
---
# <a name="patching-selected-regions-of-a-file"></a>Patchen ausgewählter Bereiche einer Datei

Beim Patchen von Dateien mit variablen Inhalten ist es möglicherweise erforderlich, die ausgewählten Bereiche der Zieldatei beizubehalten, um den Verlust kritischer Informationen zu verhindern. Beispielsweise Stempeln einige Anwendungen Benutzerinformationen in die ausführbare Datei. Da der Inhalt der Zieldatei von dem Computer abhängig sein kann, auf dem die Anwendung installiert ist, wird es schwierig zu bestimmen, ob eine bestimmte Datei ein gültiges Ziel für den Patch ist. Benutzerinformationen, die in der Zieldatei geschrieben wurden, können auch von einem Patch überschrieben werden.

Wenn Sie eine PCP-Datei (Patch Creation Properties) mit [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL](patchwiz-dll.md)generieren, können Sie angeben, dass die Informationen in bestimmten Regionen der Zieldatei beim Patchen ignoriert werden. Sie können auch angeben, dass Informationen in anderen Regionen der Zieldatei beibehalten und an einen Offset Speicherort in der aktualisierten Datei kopiert werden. Sie geben an, welche Bereiche der Zieldatei ignoriert werden sollen und welche Bereiche beibehalten werden sollen, wenn Sie die Tabellen " [targetfiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)", " [externalfiles](externalfiles-table-patchwiz-dll-.md)" und " [familyfileranmit](familyfileranges-table-patchwiz-dll-.md) " erstellen.

Verwenden Sie die Spalte retainoffsets der Tabelle " [targetfiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) " und die Spalten "retainoffsets" und "retainlängen" der Tabelle " [familyfileranges](familyfileranges-table-patchwiz-dll-.md) ", um einen Bereich von Informationen aus der Zieldatei in einen Offset Bereich in der aktualisierten Datei zu kopieren. Die Informationen in diesem Bereich werden beibehalten. Geben Sie die Länge des Bereichs mithilfe der retainlängen-Spalten der familyfileranges-Tabelle an. Die Länge des beibehaltenen Bereichs ist in den Ziel-und aktualisierten Dateien identisch. Geben Sie den Offset des Bereichs in der Zieldatei mithilfe der Spalte retainoffsets der Tabelle "targetfiles OptionalData" an. Geben Sie den Offset des Bereichs in der aktualisierten Datei mithilfe der retainoffsets-Spalte der familyfileranges-Tabelle an. Der Bereich der beibehaltenen Zieldatei ist daher der Wert von retainoffsets in der Tabelle "targetfiles OptionalData" Plus "retainlängen". Diese Informationen werden in die Update Datei in dem Bereich kopiert, der durch den Wert von retainoffsets in den Tabellen "familyfileranges" Plus "retainlängen" angegeben wird. Sie können mehrere Bereiche angeben, aber die Reihenfolge der Längen muss mit der Reihenfolge der Offsets identisch sein.

Verwenden Sie die Tabelle " [targetfiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) ", um einen Bereich der Zieldatei zu ignorieren. Informationen in diesem Bereich der Zieldatei können vom Patch weiterhin überschrieben werden. Geben Sie den Offset des Bereichs in der ignoreoffsets-Spalte und deren Länge in der ignorelengths-Spalte an. Sie können mehrere Bereiche angeben, aber die Reihenfolge der Längen muss mit der Reihenfolge der Offsets identisch sein.

Die Werte in den Längen-und Offsets-Spalten können Dezimal oder hexadezimal sein. [PATCHWIZ.DLL](patchwiz-dll.md) behandelt den Wert als hexadezimal, wenn der Wert "0x" vorangestellt ist. Die Spalten sind Zeichen folgen Spalten, sodass PATCHWIZ.DLL die Werte in ulongs konvertiert. Die Spalte Länge gibt die Länge in Bytes an.

 

 



