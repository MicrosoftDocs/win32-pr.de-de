---
description: Das SelectionTree-Steuerelement verwendet das selectionsize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: Selectionsize-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216353"
---
# <a name="selectionsize-controlevent"></a>Selectionsize-ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionsize-Ereignis, um die Größe des hervorgehobenen Elements zu veröffentlichen. Wenn es sich um ein übergeordnetes Element handelt, wird auch die Anzahl der ausgewählten untergeordneten Elemente veröffentlicht. Die Zeichenfolge ist eine der Zeichen folgen **selchildcostpos**, **selchildcostneg**, **selbientcostpospos**, **selbientcostposneg**, **selbientcostnegpos** oder **selparameentcostnegneg** aus der [UIText-Tabelle](uitext-table.md). Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das SelectionTree-Steuerelement befinden.

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie das SelectionTree-Steuerelement über die [EventMapping-Tabelle](eventmapping-table.md). Das Text Steuerelement verwendet dieses Ereignis, um die Größe des hervorgehobenen Elements anzuzeigen.

 

 



