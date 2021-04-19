---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehler Dialogfeld.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Fehler Dialogfeld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353138"
---
# <a name="error-dialog-style-bit"></a>Fehler Dialogfeld-Stilbit

Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehler Dialogfeld.

Es können mehrere Dialogfelder mit diesem Stil vorhanden sein. Die **ErrorDialog** -Eigenschaft bestimmt, welches Dialogfeld als Fehler Dialogfeld verwendet wird. Bei dem ausgewählten Dialogfeld kann es sich nur um einen Benutzer handeln, für den dieses Stilbit festgelegt ist. Das Fehler Dialogfeld muss über ein statisches Text Steuerelement namens ErrorText verfügen. Dieses Steuerelement empfängt den Text der Fehlermeldung. Das Dialogfeld sollte auch über die sieben pushschaltflächen verfügen, die den möglichen Rückgabe Werten entsprechen. Die Fehlermeldung bestimmt, welche dieser Schaltflächen tatsächlich angezeigt werden. Die angezeigten Schaltflächen werden neu angeordnet, sodass Sie im Dialogfeld gleichmäßig verteilt werden. Diese Neuanordnung ändert die X-Koordinate der Schaltflächen, jedoch nicht die anderen drei Koordinaten. Daher ist es ratsam, dass kein anderes Steuerelement im selben horizontalen Bereich des Dialog Felds wie die Schaltflächen erstellt wird. Wenn in der Fehlermeldung keine Schaltfläche angegeben ist, wird die Schaltfläche **OK** angezeigt. Die **Standard** Schaltfläche, die ersten aktiven Steuerelemente und Schaltflächen Werte **Abbrechen** werden bei einem Fehler Dialogfeld ignoriert. Die in der Fehlermeldung definierte **Standard** Schaltfläche wird allen drei Werten zugewiesen. Der Effekt, dass diese Schaltflächen gedrückt werden, muss in der [ControlEvent-Tabelle](controlevent-table.md) genau wie für alle anderen Schaltflächen definiert werden. Der Titel des Dialog Felds wird auf eine Weise erstellt, die anderen Dialogfeldern ähnelt. Sie kann von der Fehlermeldung überschrieben werden, wenn Sie einen Header Text nach der Schaltflächen Liste angibt.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbdialogattributeserror** |



 

 

 



