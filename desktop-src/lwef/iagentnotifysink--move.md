---
title: Iagentnotifysink verschieben
description: Iagentnotifysink verschieben
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948020"
---
# <a name="iagentnotifysinkmove"></a>Iagentnotifysink:: Move

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Benachrichtigt eine Client Anwendung, wenn das Zeichen verschoben wurde.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, das verschoben wurde.

</dd> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links). Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links). Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*
</dt> <dd>

Die Ursache für die Zeichen Verschiebung. Der Parameter kann eines der folgenden sein:



| Wert                                                          | BESCHREIBUNG                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Konstante **Ganzzahl ohne Vorzeichen Short neververschost** **= 0;**<br/>        | Das Zeichen wurde nicht verschoben.                                                        |
| " **Ganzzahl ohne Vorzeichen Short userverschost** " **= 1;**<br/>         | Der Benutzer hat das Zeichen gezogen.                                                          |
| " **Ganzzahl ohne Vorzeichen Short Program verschost** " **= 2;**<br/>      | Die Anwendung hat das Zeichen verschoben.                                                |
| Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogrambewegt = 3;**<br/> | Das Zeichen wurde von einer anderen Anwendung verschoben.                                             |
| **Ganzzahl ohne Vorzeichen Short** **systemverschost = 4**<br/>        | Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren. |



 

</dd> </dl>

Dieses Ereignis wird an alle Clients des Zeichens gesendet.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: getmuvecause**](iagentcharacter--getmovecause.md), [ **iagentcharacter:: muveto**](iagentcharacter--moveto.md)


 

 





