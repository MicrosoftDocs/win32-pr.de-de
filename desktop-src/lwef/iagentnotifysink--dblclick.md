---
title: Iagentnotifysink DblClick
description: Iagentnotifysink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388313"
---
# <a name="iagentnotifysinkdblclick"></a>Iagentnotifysink::D blclick

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Benachrichtigt eine Client Anwendung, wenn der Benutzer auf ein Zeichen doppelklickt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, auf das Doppel geklickt wird.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*"f"-Schlüssel*
</dt> <dd>

Ein-Parameter, der den Mauszeiger-und modifiziererschlüsselzustand angibt. Der-Parameter kann eine beliebige Kombination der folgenden zurückgeben:



|        |                                                |
|--------|------------------------------------------------|
| 0x0001 | Linke Schaltfläche                                    |
| 0x0010 | Mittlere Schaltfläche                                  |
| 0x0002 | Rechte Schaltfläche                                   |
| 0x0004 | Umschalttaste nach unten                                 |
| 0x0008 | Steuerelement Taste unten                               |
| 0x0020 | Alt-Taste unten                                   |
| 0x1000 | Das Ereignis ist auf dem Task leisten Symbol des Zeichens aufgetreten. |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> </dl>

Dieses Ereignis wird an den Eingabe aktiven Client des Zeichens gesendet. Wenn keiner der Clients des Zeichens Eingabe aktiv ist, benachrichtigt der Server den aktiven Client des Zeichens. Wenn das Zeichen sichtbar ist, bewirkt der Server, dass der Client die Eingabe aktiv durchführt, und sendet [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md). Wenn das Zeichen ausgeblendet ist, wird das Zeichen ebenfalls automatisch angezeigt.

 

 




