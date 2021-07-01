---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119684"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

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



| Wert                                                               | Beschreibung                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Das Zeichen wurde nicht verschoben.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | Der Benutzer hat das Zeichen gezogen.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | Die Anwendung hat das Zeichen verschoben.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Das Zeichen wurde von einer anderen Anwendung verschoben.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm zu halten. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentNotifySink::Move**](iagentnotifysink--move.md)


 

 





