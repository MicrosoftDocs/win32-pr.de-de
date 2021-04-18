---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, während das vorhandene Dialogfeld weiterhin ausgeführt wird, dass eine Funktion oder alle Features lokal ausgeführt werden sollen.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: ADDLOCAL-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347548"
---
# <a name="addlocal-controlevent"></a>ADDLOCAL-ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, während das vorhandene Dialogfeld weiterhin ausgeführt wird, dass eine Funktion oder alle Features lokal ausgeführt werden sollen. Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, entweder der Name der Funktion oder "All".

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um das Installationsprogramm zu benachrichtigen, ohne das Dialogfeld zu beenden.

 

 



