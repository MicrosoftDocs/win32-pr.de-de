---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120805"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer das Ziehen eines Zeichens beendet.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des gezogenen Zeichens.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Ein Parameter, der den Zustand der Maustaste und des Modifizierers angibt. Der -Parameter kann eine beliebige Kombination der folgenden Punkte zurückgeben:



| Wert  | Beschreibung      |
|--------|------------------|
| 0x0001 | Linke Schaltfläche      |
| 0x0010 | Mittlere Schaltfläche    |
| 0x0002 | Rechte Schaltfläche     |
| 0x0004 | UMSCHALTTASTE NACH UNTEN   |
| 0x0008 | Steuertaste nach unten |
| 0x0020 | ALT-TASTE NACH UNTEN     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> </dl>

 

 




