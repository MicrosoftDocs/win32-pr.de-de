---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d0f695fb1d183cced20609fc70abc0bfca0e51ddf2f904ae320a6c4844f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962276"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Ruft die Ursache der letzten Bewegung des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Die Adresse einer Variablen, die die Ursache für die letzte Bewegung des Zeichens empfängt und eine der folgenden Variablen ist:



| Wert                                                               | BESCHREIBUNG                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Das Zeichen wurde nicht verschoben.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | Der Benutzer hat das Zeichen gezogen.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | Die Anwendung hat das Zeichen verschoben.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Das Zeichen wurde von einer anderen Anwendung verschoben.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm zu halten. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentNotifySink::Move**](iagentnotifysink--move.md)


 

 





