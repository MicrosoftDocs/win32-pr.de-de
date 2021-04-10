---
description: Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen. Der Name kann in einem Dialogfeld durch ein Text Steuerelement angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: Action Text ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959551"
---
# <a name="actiontext-controlevent"></a>Action Text ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um den Namen der aktuellen Aktion zu veröffentlichen. Der Name kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Die Abonnenten werden angezeigt, wenn eine neue Fortschritts Daten vom Installationsprogramm empfangen werden.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md). Das [Text Steuer](text-control-attribute.md) Element-Attribut sollte im Feld Attribute der Tabelle aufgelistet werden, um den Namen der aktuellen Aktion zu erhalten.

 

 



