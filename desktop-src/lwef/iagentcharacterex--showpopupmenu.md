---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67d01edae103bad10eb085c4bfd1f5ce559bf26ab030816d241367ec3c13763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105458"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Zeigt das Popupmenü für das Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate des Popupmenüs des Zeichens in Pixel relativ zum Ursprung des Bildschirms (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate des Popupmenüs des Zeichens in Pixel relativ zum Bildschirmursprung (oben links).

</dd> </dl>

Wenn Sie [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) auf **False** festlegen, zeigt der Server das Menü nicht mehr automatisch an, wenn mit der rechten Maustaste auf das Zeichen oder sein Taskleistensymbol geklickt wird. Sie können diese Methode verwenden, um das Menü anzuzeigen.

Das Menü wird angezeigt, bis der Benutzer einen Befehl oder ein anderes Menü auswählt. Es kann jeweils nur ein Popupmenü angezeigt werden. Daher werden Aufrufe dieser Methode das vorherige Menü abbrechen (entfernen).

Diese Methode sollte nur aufgerufen werden, wenn Ihre Clientanwendung der aktive Client des Zeichens ist. andernfalls schlägt der Fehler fehl.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




