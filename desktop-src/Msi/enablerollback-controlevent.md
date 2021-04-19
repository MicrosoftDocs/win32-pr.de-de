---
description: Diese ControlEvent kann zum Aktivieren oder Deaktivieren der Rollback-Funktionen des Installers verwendet werden.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: Enablerollback-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345830"
---
# <a name="enablerollback-controlevent"></a>Enablerollback-ControlEvent

Diese ControlEvent kann zum Aktivieren oder Deaktivieren der Rollback-Funktionen des Installers verwendet werden.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

False deaktiviert die Rollback-Funktionen des Installers. True schaltet die Rollback-Funktionen des Installers um.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Kann verwendet werden, um die Rollback-Funktionen zu deaktivieren, wenn der Installer erkennt, dass nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen. In diesem Fall sollte ControlEvent mit den Eigenschaften [**ouesfdiskspace**](outofdiskspace.md), [**outo fnorbdiskspace**](outofnorbdiskspace.md)und [**promptrollbackcost**](promptrollbackcost.md) verwendet werden.

 

 



