---
description: Das SelectionTree-Steuerelement verwendet das selectionpathon-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahl Pfad zugeordnet ist. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: Selectionpathon ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359601"
---
# <a name="selectionpathon-controlevent"></a>Selectionpathon ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionpathon-Ereignis, um einen booleschen Wert zu veröffentlichen, der angibt, ob dem aktuell ausgewählten Feature ein Auswahl Pfad zugeordnet ist. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Der seleclevent "selectionpathon" wird nie während einer [Wartungs Installation](maintenance-installation.md)veröffentlicht.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren. Das Text Steuerelement zeigt die Beschriftung des Auswahl Pfads an. Dieses Text Steuerelement ist abhängig vom Ereignis sichtbar oder ausgeblendet.

 

 



