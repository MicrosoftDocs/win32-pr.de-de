---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120923"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer auf ein Zeichen doppelklickt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des doppelgeklickten Zeichens.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Ein Parameter, der den Zustand der Maustaste und des Modifiziererschlüssels angibt. Der -Parameter kann eine beliebige Kombination der folgenden Angaben zurückgeben:



| Wert  | Beschreibung                               |
|--------|------------------------------------------------|
| 0x0001 | Linke Schaltfläche                                    |
| 0x0010 | Mittlere Schaltfläche                                  |
| 0x0002 | Schaltfläche "Rechts"                                   |
| 0x0004 | UMSCHALTTASTE NACH-UNTEN                                 |
| 0x0008 | Steuerungsschlüssel nach unten                               |
| 0x0020 | ALT-TASTE NACH-UNTEN                                   |
| 0x1000 | Das Ereignis ist auf dem Taskleistensymbol des Zeichens aufgetreten. |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirmursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirmursprung (oben links).

</dd> </dl>

Dieses Ereignis wird an den eingabeaktiven Client des Zeichens gesendet. Wenn keiner der Clients des Zeichens eingabeaktiv ist, benachrichtigt der Server den aktiven Client des Zeichens. Wenn das Zeichen sichtbar ist, aktiviert der Server auch den Client input-active und sendet [**IAgentNotifySink::ActivateInputState.**](iagentnotifysink--activateinputstate.md) Wenn das Zeichen ausgeblendet ist, wird es auch automatisch angezeigt.

 

 




