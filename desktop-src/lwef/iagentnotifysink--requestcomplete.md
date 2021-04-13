---
title: Iagentnotifysink requestcomplete
description: Iagentnotifysink requestcomplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311040"
---
# <a name="iagentnotifysinkrequestcomplete"></a>Iagentnotifysink:: requestcomplete

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Benachrichtigt eine Client Anwendung, wenn eine Anforderung abgeschlossen ist.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwrequestid*
</dt> <dd>

Der Bezeichner der Anforderung, die gestartet wurde.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

Statuscode. Dieser Parameter gibt den Statuscode für die Anforderung zurück.

</dd> </dl>

Mithilfe dieses Ereignisses können Sie nachverfolgen, wann eine in der Warteschlange stehende Methode mithilfe ihrer Anforderungs-ID abgeschlossen wird.

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysink:: requeststart**](iagentnotifysink--requeststart.md), [**iagent:: Load**](iagent--load.md), [**iagentcharacter:: gestureat**](iagentcharacter--gestureat.md), [**iagentcharacter:: Hide**](iagentcharacter--hide.md), [**iagentcharacter:: Interrupt**](iagentcharacter--interrupt.md), [**iagentcharacter:: muveto**](iagentcharacter--moveto.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md), [**iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentcharacter:: Show**](iagentcharacter--show.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md), [**iagentcharacter:: Wait**](iagentcharacter--wait.md)


 

 




