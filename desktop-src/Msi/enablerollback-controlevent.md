---
description: Dieses ControlEvent kann verwendet werden, um die Rollbackfunktionen des Installationsprogramms zu aktivieren oder zu deaktivieren.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143111"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent

Dieses ControlEvent kann verwendet werden, um die Rollbackfunktionen des Installationsprogramms zu aktivieren oder zu deaktivieren.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

False deaktiviert die Rollbackfunktionen des Installationsprogramms. True aktiviert die Rollbackfunktionen des Installationsprogramms.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Kann verwendet werden, um Rollbackfunktionen zu deaktivieren, wenn das Installationsprogramm erkennt, dass nicht genügend Speicherplatz verfügbar ist, um die Installation abzuschließen. In diesem Fall sollte ControlEvent mit den Eigenschaften [**OutOfDiskSpace,**](outofdiskspace.md) [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)und [**PROMPTROLLBACKCOST**](promptrollbackcost.md) verwendet werden.

 

 



