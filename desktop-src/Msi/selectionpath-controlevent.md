---
description: Das SelectionTree-Steuerelement verwendet das SelectionPath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45dfcb017c18b026f03bf9fa9b89d7be33db49bafc3dd9f899846cbada1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040440"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent

Das [SelectionTree-Steuerelement](selectiontree-control.md) verwendet das SelectionPath-Ereignis, um den Pfad für das hervorgehobene Element zu veröffentlichen. Wenn das Element für die Ausführung aus der Quelle ausgewählt ist, ist dies der Pfad der Quelle. Wenn das Element als nicht vorhanden ausgewählt ist, ist die Zeichenfolge die **AbsentPath-Zeichenfolge** aus der [UIText-Tabelle](uitext-table.md). Dieses Ereignis sollte in der [EventMapping-Tabelle verfasst werden.](eventmapping-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text-Steuerelement](text-control.md) im gleichen modalen Dialogfeld wie selectionTree sollte das Ereignis über die [EventMapping-Tabelle abonnieren.](eventmapping-table.md) Das Textsteuerelement zeigt den Pfad des hervorgehobenen Elements an.

 

 



