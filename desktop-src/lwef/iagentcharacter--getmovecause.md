---
title: Iagentcharacter getmuvecause
description: Iagentcharacter getmuvecause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388813"
---
# <a name="iagentcharactergetmovecause"></a>Iagentcharacter:: getmuvecause

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Ruft die Ursache für den letzten Verschiebe Vorgang des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwcause*
</dt> <dd>

Adresse einer Variablen, die die Ursache des letzten Verschiebens des Zeichens empfängt und eine der folgenden ist:



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Konstante **Ganzzahl ohne Vorzeichen Short neververschost** **= 0;**<br/>        | Das Zeichen wurde nicht verschoben.                                                        |
| " **Ganzzahl ohne Vorzeichen Short userverschost** " **= 1;**<br/>         | Der Benutzer hat das Zeichen gezogen.                                                          |
| " **Ganzzahl ohne Vorzeichen Short Program verschost** " **= 2;**<br/>      | Die Anwendung hat das Zeichen verschoben.                                                |
| Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogrambewegt = 3;**<br/> | Das Zeichen wurde von einer anderen Anwendung verschoben.                                             |
| **Ganzzahl ohne Vorzeichen Short** **systemverschost = 4**<br/>        | Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysink:: Move**](iagentnotifysink--move.md)


 

 





