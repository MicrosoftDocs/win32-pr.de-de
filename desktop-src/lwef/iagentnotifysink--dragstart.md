---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3510449923d4567d3126bf9cd84655acd782b021f9f37f655a51114122a4717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105214"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink::D ragStart

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.

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

 

 




