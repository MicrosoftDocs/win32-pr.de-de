---
title: Iagentcharakteriex showPopupMenu
description: Iagentcharakteriex showPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856479"
---
# <a name="iagentcharacterexshowpopupmenu"></a>Iagentcharakteriex:: showPopupMenu

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Zeigt das Popup Menü für das Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate des Popup Menüs des Zeichens in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate des Popup Menüs des Zeichens in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> </dl>

Wenn Sie [**iagentcharakteriex:: setautopopupmenu**](iagentcharacterex--setautopopupmenu.md) auf **false** festlegen, wird das Menü vom Server nicht mehr automatisch angezeigt, wenn mit der rechten Maustaste auf das Zeichen oder das zugehörige Symbol der Taskleiste geklickt wird. Mit dieser Methode können Sie das Menü anzeigen.

Das Menü wird angezeigt, bis der Benutzer einen Befehl auswählt oder ein anderes Menü anzeigt. Es kann jeweils nur ein Popup Menü angezeigt werden. Daher wird durch Aufrufe dieser Methode das erste Menü abgebrochen (entfernt).

Diese Methode sollte nur aufgerufen werden, wenn die Client Anwendung der aktive Client des Zeichens ist. Andernfalls tritt ein Fehler auf.

[**Iagentcharakteriex:: abtautopopupmenu**](iagentcharacterex--setautopopupmenu.md)

 

 




