---
description: 'Das Dialogfeld wird zurückgesetzt. Anders ausgedrückt: Alle Steuerelemente im Dialogfeld werden aufgerufen, um die vorgenommenen Eigenschaftsänderungen rückgängig zu machen. Dieses Ereignis setzt alle Eigenschaftswerte auf den Wert zurück, den sie beim Erstellen des Dialogfelds hatten.'
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: ControlEvent zurücksetzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adcd67a0511c8d500064e8816211cbc445d0e112d3a5156fbc6f0590637e09c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990312"
---
# <a name="reset-controlevent"></a>ControlEvent zurücksetzen

Das Dialogfeld wird zurückgesetzt. Anders ausgedrückt: Alle Steuerelemente im Dialogfeld werden aufgerufen, um die vorgenommenen Eigenschaftsänderungen rückgängig zu machen. Dieses Ereignis setzt alle Eigenschaftswerte auf den Wert zurück, den sie beim Erstellen des Dialogfelds hatten.

Dieses Ereignis kann von einem [PushButton-Steuerelement oder einem](pushbutton-control.md) [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Es gibt einen Fall, der selten in der Praxis auftreten sollte, der von diesem ControlEvent nicht ordnungsgemäß behandelt wird. Wenn zwei oder mehr Steuerelemente im gleichen Dialogfeld indirekt mit derselben Eigenschaft verknüpft sind und mindestens eines davon mit einer anderen Eigenschaft begonnen hat, wird dieser Eigenschaftswert manchmal auf den zweiten Wert zurückgesetzt.

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld wird verwendet, um alle Werte im Dialogfeld zurückzusetzen und alle Änderungen auf der Seite abzubricht.

 

 



