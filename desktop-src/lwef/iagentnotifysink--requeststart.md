---
title: Iagentnotifysink requeststart
description: Iagentnotifysink requeststart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713620"
---
# <a name="iagentnotifysinkrequeststart"></a>Iagentnotifysink:: requeststart

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

Benachrichtigt eine Client Anwendung, wenn eine Anforderung beginnt.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwrequestid*
</dt> <dd>

Der Bezeichner der Anforderung, die gestartet wurde.

</dd> </dl>

Mithilfe dieses Ereignisses können Sie nachverfolgen, wann eine Anforderung in der Warteschlange mit ihrer Anforderungs-ID beginnt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentnotifysink:: requestcomplete**](iagentnotifysink--requestcomplete.md), [**iagent:: Load**](iagent--load.md), [**iagentcharacter:: gestureat**](iagentcharacter--gestureat.md), [**iagentcharacter:: Hide**](iagentcharacter--hide.md), [**iagentcharacter:: Interrupt**](iagentcharacter--interrupt.md), [**iagentcharacter:: muveto**](iagentcharacter--moveto.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md), [**iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentcharacter:: Show**](iagentcharacter--show.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md), [**iagentcharacter:: Wait**](iagentcharacter--wait.md)


 

 




