---
description: Das ValidateProductID-Ereignis legt die ProductID-Eigenschaft auf die vollständige Produkt-ID fest. Wenn die Überprüfung nicht erfolgreich ist, wird durch dieses Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae9ae5747deb9995c2e33a5c44541793442be8844b224c28c8a91e412cb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786660"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent

Das ValidateProductID-Ereignis legt die [**ProductID-Eigenschaft**](productid.md) auf die vollständige Produkt-ID fest. Wenn die Überprüfung nicht erfolgreich ist, wird durch dieses Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.

Dieses Ereignis kann von einem [PushButton-Steuerelement oder einem](pushbutton-control.md) [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um den Benutzereintrag der Produkt-ID zu überprüfen. Wenn der Eintrag des Benutzers gültig ist, wird das nächste Dialogfeld geöffnet.

 

 



