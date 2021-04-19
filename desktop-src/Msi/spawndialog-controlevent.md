---
description: Das handlevent spawndialog benachrichtigt den Installer, ein untergeordnetes Element eines modalen Dialog Felds zu erstellen, während das vorhandene Dialogfeld weiterhin ausgeführt wird.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: Spawndialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346688"
---
# <a name="spawndialog-controlevent"></a>Spawndialog-ControlEvent

Das handlevent spawndialog benachrichtigt den Installer, ein untergeordnetes Element eines modalen Dialog Felds zu erstellen, während das vorhandene Dialogfeld weiterhin ausgeführt wird.

Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden. Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, bei der es sich um den Namen des neuen Dialog Felds handelt.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um ein untergeordnetes Dialogfeld zu erstellen, z. b. "möchten Sie den Vorgang wirklich abbrechen?" .

 

 



