---
title: IAgentNotifySink Move
description: IAgentNotifySink Move
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105174"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink::Move

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Benachrichtigt eine Clientanwendung, wenn das Zeichen verschoben wurde.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des verschobenen Zeichens.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirmursprung (oben links). Die Position eines Zeichens basiert auf der oberen linken Ecke des Animationsrahmens.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirmursprung (oben links). Die Position eines Zeichens basiert auf der oberen linken Ecke des Animationsrahmens.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Die Ursache des Zeichenverschiebens. Der -Parameter kann eine der folgenden Sein:



| Wert                                                          | Beschreibung                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Das Zeichen wurde nicht verschoben.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | Der Benutzer hat das Zeichen gezogen.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | Die Anwendung hat das Zeichen verschoben.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Eine andere Anwendung hat das Zeichen verschoben.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | Der Server hat das Zeichen verschoben, damit es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm angezeigt wird. |



 

</dd> </dl>

Dieses Ereignis wird an alle Clients des Zeichens gesendet.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)


 

 





