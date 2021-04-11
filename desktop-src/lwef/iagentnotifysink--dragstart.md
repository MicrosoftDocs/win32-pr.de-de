---
title: Iagentnotifysink DragStart
description: Iagentnotifysink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310079"
---
# <a name="iagentnotifysinkdragstart"></a>Iagentnotifysink::D ragstart

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Benachrichtigt eine Client Anwendung, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des gezogenen Zeichens.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*"f"-Schlüssel*
</dt> <dd>

Ein-Parameter, der den Mauszeiger-und modifiziererschlüsselzustand angibt. Der-Parameter kann eine beliebige Kombination der folgenden zurückgeben:



|        |                  |
|--------|------------------|
| 0x0001 | Linke Schaltfläche      |
| 0x0010 | Mittlere Schaltfläche    |
| 0x0002 | Rechte Schaltfläche     |
| 0x0004 | Umschalttaste nach unten   |
| 0x0008 | Steuerelement Taste unten |
| 0x0020 | Alt-Taste unten     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> </dl>

 

 




