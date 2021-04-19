---
description: Das Dialogfeld wird zurückgesetzt. Anders ausgedrückt werden alle Steuerelemente im Dialogfeld aufgerufen, um die von Ihnen durchgeführten Eigenschaften Änderungen rückgängig zu machen. Dieses Ereignis setzt alle Eigenschaftswerte auf die Elemente zurück, die beim Erstellen des Dialog Felds aufgetreten sind.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: ControlEvent zurücksetzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349300"
---
# <a name="reset-controlevent"></a>ControlEvent zurücksetzen

Das Dialogfeld wird zurückgesetzt. Anders ausgedrückt werden alle Steuerelemente im Dialogfeld aufgerufen, um die von Ihnen durchgeführten Eigenschaften Änderungen rückgängig zu machen. Dieses Ereignis setzt alle Eigenschaftswerte auf die Elemente zurück, die beim Erstellen des Dialog Felds aufgetreten sind.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Es gibt einen Fall, der in der Praxis selten auftreten sollte und von diesem ControlEvent nicht ordnungsgemäß behandelt wird. Wenn im gleichen Dialogfeld zwei oder mehr Steuerelemente vorhanden sind, die indirekt mit der gleichen Eigenschaft verknüpft sind, und mindestens eine von Ihnen mit einer anderen Eigenschaft begonnen hat, wird dieser Eigenschafts Wert manchmal auf den zweiten Wert zurückgesetzt.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld wird verwendet, um alle Werte im Dialogfeld zurückzusetzen und alle Änderungen auf der Seite abzubrechen.

 

 



