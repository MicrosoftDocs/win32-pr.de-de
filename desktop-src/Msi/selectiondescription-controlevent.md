---
description: Das SelectionTree-Steuerelement verwendet das selectiondescription-Ereignis, um eine Zeichenfolge zu veröffentlichen, die die Beschreibung für das hervorgehobene Element enthält. Diese Zeichenfolge ist das Beschreibungsfeld der Feature-Tabelle. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: Selectiondescription ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357815"
---
# <a name="selectiondescription-controlevent"></a>Selectiondescription ControlEvent

Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectiondescription-Ereignis, um eine Zeichenfolge zu veröffentlichen, die die Beschreibung für das hervorgehobene Element enthält. Diese Zeichenfolge ist das **Beschreibungs** Feld der [Feature-Tabelle](feature-table.md). Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Dieses Ereignis kann sich nur auf Steuerelemente auswirken, die sich im gleichen Dialogfeld wie das [SelectionTree-Steuer](selectiontree-control.md)Element befinden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Keine.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [Text](text-control.md) Steuerelement im gleichen modalen Dialogfeld wie SelectionTree abonniert dieses ControlEvent über die [EventMapping-Tabelle](eventmapping-table.md). Das Text Steuerelement verwendet dieses Ereignis, um die Beschreibung des hervorgehobenen Elements anzuzeigen.

 

 



