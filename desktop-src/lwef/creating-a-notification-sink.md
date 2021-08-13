---
title: Erstellen einer Benachrichtigungssenke
description: Erstellen einer Benachrichtigungssenke
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480092"
---
# <a name="creating-a-notification-sink"></a>Erstellen einer Benachrichtigungssenke

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Um vom Microsoft-Agent über Ereignisse benachrichtigt zu werden, müssen Sie entweder die [**IAgentNotifySink-**](events.md)oder die [**IAgentNotifySinkEx-Schnittstelle**](iagentnotifysinkex.md) implementieren und ein Objekt dieses Typs gemäß den COM-Konventionen erstellen und registrieren:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Denken Sie daran, die Registrierung Ihrer Benachrichtigungssenke zu aufheben, wenn Ihre Anwendung heruntergefahren und die Schnittstellen des Microsoft-Agents veröffentlicht wird.

 

 




