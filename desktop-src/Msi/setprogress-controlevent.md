---
description: Das Installationsprogramm verwendet das SetProgress-Ereignis, um Informationen zum Installationsfortschritt zu veröffentlichen.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625080"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent

Das Installationsprogramm verwendet das SetProgress-Ereignis, um Informationen zum Installationsfortschritt zu veröffentlichen. Ein [ProgressBar-Steuerelement](progressbar-control.md) oder ein Steuerelement vom Status ["Steuerelement"](billboard-control.md) sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) abonnieren, indem die Aktion, deren Fortschritt angegeben wird, genannt wird. Dieses Ereignis sollte in der [EventMapping-Tabelle verfasst werden.](eventmapping-table.md)

Dieses ControlEvent kann von einer Benutzeroberfläche [](b-gly.md)verarbeitet werden, die auf der einfachen Benutzeroberfläche, auf einer reduzierten [*Benutzeroberfläche*](r-gly.md)oder auf [*vollständigen Benutzeroberflächenebenen ausgeführt*](f-gly.md) wird. Informationen zu Benutzeroberflächenebenen finden Sie unter [Benutzeroberfläche Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [ProgressBar-Steuerelement](progressbar-control.md) in einem nicht moduslosen Dialogfeld abonniert dieses Ereignis mithilfe des Progress-Attributs, um die Statusinformationen zu empfangen. [](progress-control-attribute.md)

 

 



