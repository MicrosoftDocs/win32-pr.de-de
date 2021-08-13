---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, während das aktuelle Dialogfeld ausgeführt wird, dass ein Feature oder alle Features lokal ausgeführt werden sollen.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb2db93bea39d167d5b8f08af2cdecfcb07194fb68d4c1e39f5511e2a09f8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639562"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, während das aktuelle Dialogfeld ausgeführt wird, dass ein Feature oder alle Features lokal ausgeführt werden sollen. Dieses Ereignis kann von einem [PushButton-Steuerelement,](pushbutton-control.md)einem [Kontrollkästchen-Steuerelement](checkbox-control.md)oder einem [SelectionTree-Steuerelement](selectiontree-control.md)veröffentlicht werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle](controlevent-table.md)erstellt werden.

Für dieses ControlEvent muss die Benutzeroberfläche auf [*der vollständigen Benutzeroberflächenebene*](f-gly.md) ausgeführt werden. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzeroberfläche*](r-gly.md) oder [*einer einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Ebenen.](user-interface-levels.md)

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, entweder der Name des Features oder "ALL".

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um das Installationsprogramm zu benachrichtigen, ohne das Dialogfeld zu beenden.

 

 



