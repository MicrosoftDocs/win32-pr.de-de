---
description: Das Installationsprogramm wird durch dieses Ereignis benachrichtigt, wenn ein Feature oder alle Funktionen zum Entfernen ausgewählt werden, während das vorhandene Dialogfeld weiterhin ausgeführt wird.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: ControlEvent entfernen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373047"
---
# <a name="remove-controlevent"></a>ControlEvent entfernen

Das Installationsprogramm wird durch dieses Ereignis benachrichtigt, wenn ein Feature oder alle Funktionen zum Entfernen ausgewählt werden, während das vorhandene Dialogfeld weiterhin ausgeführt wird.

Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, die entweder der Name der Funktion oder "All" ist.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="action-by-publisher-when-subscriber-activated"></a>Aktion nach Verleger beim Aktivieren des Abonnenten

Das Installationsprogramm speichert das vorhandene Dialogfeld und benachrichtigt das Installationsprogramm.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld, das an dieses Ereignis gebunden ist.

 

 



