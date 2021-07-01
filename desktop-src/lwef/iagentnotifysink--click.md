---
title: IAgentNotifySink-Klick
description: IAgentNotifySink-Klick
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120903"
---
# <a name="iagentnotifysinkclick"></a>IAgentNotifySink::Click

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer auf das Taskleistensymbol eines Zeichens oder Zeichens klickt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des geklickten Zeichens.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Ein Parameter, der den Zustand der Maustaste und des Modifizierers angibt. Der -Parameter kann eine beliebige Kombination der folgenden Punkte zurückgeben:



| Wert  | Beschreibung                                    |
|--------|------------------------------------------------|
| 0x0001 | Linke Schaltfläche                                    |
| 0x0010 | Mittlere Schaltfläche                                  |
| 0x0002 | Rechte Schaltfläche                                   |
| 0x0004 | UMSCHALTTASTE NACH UNTEN                                 |
| 0x0008 | Steuertaste nach unten                               |
| 0x0020 | ALT-TASTE NACH UNTEN                                   |
| 0x1000 | Das Ereignis ist auf dem Taskleistensymbol des Zeichens aufgetreten. |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> </dl>

Dieses Ereignis wird an den eingabeaktiven Client des Zeichens gesendet. Wenn keiner der Clients des Zeichens eingabeaktiv ist, benachrichtigt der Server den aktiven Client des Zeichens. Wenn das Zeichen sichtbar ist, macht der Server diesen Client auch eingabeaktiv und sendet [**den IAgentNotifySink::ActivateInputState.**](iagentnotifysink--activateinputstate.md) Wenn das Zeichen ausgeblendet ist, wird das Zeichen ebenfalls automatisch angezeigt.

 

 




