---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehlerdialogfeld.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Error Dialog Style Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f9c244e0f7905b72faf53306a7556ac8f9bb718c48666630751a5c0b20762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913490"
---
# <a name="error-dialog-style-bit"></a>Error Dialog Style Bit

Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehlerdialogfeld.

Es kann mehrere Dialoge mit diesem Stil geben. Die **ErrorDialog-Eigenschaft** bestimmt, welcher Dialog als Fehlerdialog verwendet wird. Das ausgewählte Dialogfeld kann nur eines der Dialogfelder sein, für die dieses Stilbit festgelegt ist. Das Fehlerdialogfeld muss über ein statisches Textsteuerelement mit dem Namen ErrorText verfügen. Dieses Steuerelement empfängt den Text der Fehlermeldung. Das Dialogfeld sollte auch über die sieben Schaltflächen verfügen, die den möglichen Rückgabewerten entsprechen. Die Fehlermeldung bestimmt, welche dieser Schaltflächen tatsächlich angezeigt werden. Die angezeigten Schaltflächen werden neu angeordnet, sodass sie gleichmäßig im Dialogfeld verteilt werden. Diese Neuordnung ändert die X-Koordinate der Schaltflächen, jedoch nicht die anderen drei Koordinaten. Daher ist es ratsam, kein anderes Steuerelement im selben horizontalen Bereich des Dialogs wie die Schaltflächen zu erstellen. Wenn in der Fehlermeldung keine Schaltfläche angegeben wird, wird die Schaltfläche **OK** angezeigt. Die Werte **für die Schaltflächen Standard,** Erstes aktives Steuerelement und **Schaltfläche abbrechen** werden für ein Fehlerdialogfeld ignoriert. Die in der Fehlermeldung definierte Schaltfläche **Standard** wird allen drei Werten zugewiesen. Die Auswirkung des Pushens dieser Schaltflächen muss in der [ControlEvent-Tabelle](controlevent-table.md) genau wie bei allen anderen Schaltflächen definiert werden. Der Titel des Dialogs wird ähnlich wie bei anderen Dialogen erstellt. Sie kann durch die Fehlermeldung überschrieben werden, wenn sie einen Headertext nach der Schaltflächenliste angibt.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



