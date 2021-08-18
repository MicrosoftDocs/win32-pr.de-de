---
description: Das SelectionTree-Steuerelement verwendet das SelectionSize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040360"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent

Das [SelectionTree-Steuerelement](selectiontree-control.md) verwendet das SelectionSize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen. Wenn es sich um ein übergeordnetes Element handelt, wird auch die Anzahl der ausgewählten übergeordneten Elemente veröffentlicht. Die Zeichenfolge ist eine der Zeichenfolgen **SelChildCostPos,** **SelChildCostNeg,** **SelParentCostPosPos,** **SelParentCostPosNeg,** **SelParentCostNegPos** oder **SelParentCostNegNeg** aus der [UIText-Tabelle.](uitext-table.md) Dieses Ereignis sollte in der [EventMapping-Tabelle verfasst werden.](eventmapping-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text-Steuerelement](text-control.md) im gleichen modalen Dialogfeld wie das SelectionTree-Steuerelement über die [EventMapping-Tabelle](eventmapping-table.md). Das Textsteuerelement verwendet dieses Ereignis, um die Größe des hervorgehobenen Elements anzuzeigen.

 

 



