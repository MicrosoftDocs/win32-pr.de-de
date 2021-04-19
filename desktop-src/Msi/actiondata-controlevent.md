---
description: Das Installationsprogramm verwendet dieses Ereignis, um Daten auf der neuesten Aktion zu veröffentlichen. Die Daten können in einem Dialogfeld durch ein Text Steuerelement angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: Aktions Daten-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367886"
---
# <a name="actiondata-controlevent"></a>Aktions Daten-ControlEvent

Das Installationsprogramm verwendet dieses Ereignis, um Daten auf der neuesten Aktion zu veröffentlichen. Die Daten können in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Die Abonnenten werden ausgeblendet, wenn eine neue Aktion startet und angezeigt wird, wenn neue Aktions Daten vom Installationsprogramm empfangen werden.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md). Das [Text Steuer](text-control-attribute.md) Element-Attribut wird im Feld Attribute der Tabelle aufgelistet, um die aktuellen Aktions Daten zu empfangen. Wird normalerweise verwendet, um die Namen der Dateien anzuzeigen, die beim Kopieren von Dateien kopiert wurden.

 

 



