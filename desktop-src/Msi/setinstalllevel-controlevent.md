---
description: Das SetInstallLevel-Ereignis ändert die Installationsebene in den vom -Argument angegebenen Wert.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7632e666dc169318e04cbcaf979aa82432d028cc6b7230e6a5e711350ef35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625108"
---
# <a name="setinstalllevel-controlevent"></a>SetInstallLevel ControlEvent

Das SetInstallLevel-Ereignis ändert die Installationsebene in den vom -Argument angegebenen Wert.

Dieses Ereignis kann von einem [PushButton-Steuerelement](pushbutton-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine ganze Zahl, die der neue Wert der Installationsebene ist.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Keine.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um die Installationsebene zu ändern.

 

 



