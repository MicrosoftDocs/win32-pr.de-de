---
description: Das SelectionTree-Steuerelement verwendet das selectionpath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: Selectionpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959925"
---
# <a name="selectionpath-controlevent"></a>Selectionpath ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionpath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen. Wenn das Element zum Ausführen aus der Quelle ausgewählt ist, ist dies der Pfad der Quelle. Wenn das Element als nicht vorhanden ausgewählt wird, ist die Zeichenfolge die **absentpath** -Zeichenfolge aus der [UIText-Tabelle](uitext-table.md). Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md)abonnieren. Das Text Steuerelement zeigt den Pfad des hervorgehobenen Elements an.

 

 



