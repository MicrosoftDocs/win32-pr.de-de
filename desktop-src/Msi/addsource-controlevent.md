---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, während der aktuelle Dialog ausgeführt wird, dass ein Feature oder alle Features aus der Quelle ausgeführt werden sollen.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0adff72ac14376c7084d6c3c005a77b2891019947cd22e8d73e58bfa09ad64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145953"
---
# <a name="addsource-controlevent"></a>AddSource ControlEvent

Dieses Ereignis benachrichtigt das Installationsprogramm, während der aktuelle Dialog ausgeführt wird, dass ein Feature oder alle Features aus der Quelle ausgeführt werden sollen. Dieses Ereignis kann von einem [PushButton-Steuerelement,](pushbutton-control.md)einem [Checkbox-Steuerelement](checkbox-control.md)oder einem [SelectionTree-Steuerelement veröffentlicht werden.](selectiontree-control.md) Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, entweder der Name des Features oder "ALL".

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um das Installationsprogramm zu benachrichtigen, ohne das Dialogfeld zu beenden.

 

 



