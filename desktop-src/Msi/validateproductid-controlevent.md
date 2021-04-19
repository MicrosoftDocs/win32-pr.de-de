---
description: Das ValidateProductID-Ereignis legt die ProductID-Eigenschaft auf die vollständige Produkt-ID fest. Wenn die Überprüfung nicht erfolgreich ist, werden mit diesem Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355519"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent

Das ValidateProductID-Ereignis legt die [**ProductID-**](productid.md) Eigenschaft auf die vollständige Produkt-ID fest. Wenn die Überprüfung nicht erfolgreich ist, werden mit diesem Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um den Benutzereintrag der Produkt-ID zu überprüfen. Wenn der Benutzereintrag gültig ist, wird das nächste Dialogfeld geöffnet.

 

 



