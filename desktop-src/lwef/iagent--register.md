---
title: IAgent-Register
description: IAgent-Register
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962670"
---
# <a name="iagentregister"></a>IAgent::Register

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registriert eine Benachrichtigungssenke für die Clientanwendung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Adresse von [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) für Ihre Benachrichtigungssenkenschnittstelle.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Adresse der Benachrichtigungssenke-ID (wird zum Aufheben der Registrierung der Benachrichtigungssenke verwendet).

</dd> </dl>

Sie müssen Ihre Benachrichtigungssenke (auch als Benachrichtigungssenke oder Ereignissenke bezeichnet) registrieren, um Ereignisse vom Microsoft-Agent-Server zu empfangen.

## <a name="see-also"></a>Weitere Informationen

[**IAgent::Unregister**](iagent--unregister.md)


 

 




