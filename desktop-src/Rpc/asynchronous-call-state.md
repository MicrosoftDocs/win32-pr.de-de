---
title: Asynchroner Aufrufzustand
description: Auf dieser Seite wird der asynchrone Aufrufzustand für RPC-Aufrufe beschrieben.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478626"
---
# <a name="asynchronous-call-state"></a>Asynchroner Aufrufzustand

Auf dieser Seite wird der asynchrone Aufrufzustand für RPC-Aufrufe beschrieben.

## <a name="client-behavior"></a>Clientverhalten




| State | Name des Zustands | Aktion | 
|-------|------------|--------|
| C | Rufen Sie auf. | Machen Sie den RPC<ul><li>Bei Erfolg zu Zustand WComp wechseln</li><li>Bei Ausnahme zu Ende wechseln</li></ul>So führen Sie einen Fehler aus: Wechseln Sie zu Kann.<br /> | 
| Kann | Abbrechen des Anrufs | Aufrufen <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>von RpcAsyncCancelCall</strong></a>Go to WComp<br /> | 
| WComp | Warten auf den Abschluss | Warten, bis notificationCall-complete notification empfangen werden soll<br /> Wechseln Sie zu "Comp".<br /> | 
| Comp | Completion | Problem: <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Zum Ende wechseln<br /> | 
| Ende | 




 

## <a name="server-behavior"></a>Serververhalten



| State | Name des Zustands     | Aktion                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | Der Aufruf wird von rpc runtimeProcess versendet.<br/> Wechseln Sie zu "Comp".<br/> To fail fatally (while executing on the RPC thread): Raise exception; Gehe zu Ende<br/> So führen Sie einen ordnungsgemäßen Fehler aus: Wechseln Sie zu A.<br/> |
| Ein     | Abbrechen des Aufrufs | Aufrufen [**von RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End<br/>                                                                                                                                             |
| Comp  | Completion     | Problem: [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Zum Ende wechseln<br/>                                                                                                                                      |
| Ende   |                |                                                                                                                                                                                                                     |



 

 

 





