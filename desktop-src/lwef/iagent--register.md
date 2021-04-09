---
title: Iagent-Register
description: Iagent-Register
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856240"
---
# <a name="iagentregister"></a>Iagent:: Register

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registriert eine Benachrichtigungs Senke für die Client Anwendung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Adresse von [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) für Ihre Notification Sink-Schnittstelle.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwsink ID*
</dt> <dd>

Adresse der Benachrichtigungs-Senke-ID (zur Aufhebung der Registrierung der Benachrichtigungs Senke).

</dd> </dl>

Sie müssen ihre Benachrichtigungs Senke (auch als Benachrichtigungs Senke oder Ereignis Senke bezeichnet) registrieren, um Ereignisse vom Microsoft-Agent-Server zu empfangen.

## <a name="see-also"></a>Weitere Informationen

[**Iagent:: Unregister**](iagent--unregister.md)


 

 




