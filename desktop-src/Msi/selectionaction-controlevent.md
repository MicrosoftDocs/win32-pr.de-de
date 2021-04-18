---
description: Das SelectionTree-Steuerelement verwendet dieses Ereignis, um eine Zeichenfolge zu veröffentlichen, die das markierte Element beschreibt. Die Zeichenfolge ist einer der &\# 0034; SEL \* & \# 0034; Zeichen folgen aus der UIText-Tabelle. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: Selectionaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354848"
---
# <a name="selectionaction-controlevent"></a>Selectionaction ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet dieses Ereignis, um eine Zeichenfolge zu veröffentlichen, die das markierte Element beschreibt. Die Zeichenfolge ist eine der "SEL"-Zeichen folgen \* aus der [UIText-Tabelle](uitext-table.md). Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie SelectionTree sollte dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren. Das Text Steuerelement zeigt die Erläuterung des ausgewählten Elements an.

 

 



