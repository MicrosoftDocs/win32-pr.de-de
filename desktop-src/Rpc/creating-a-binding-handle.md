---
title: Erstellen eines Bindungs Handles
description: Das Client Programm einer verteilten Anwendung muss ein Bindungs Handle erstellen, das der RPC-Laufzeit mitteilt, mit welchem Server eine Verbindung hergestellt werden soll und wie eine Verbindung mit dem Server hergestellt werden soll.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Erstellen eines Bindungs Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036666"
---
# <a name="creating-a-binding-handle"></a>Erstellen eines Bindungs Handles

Das Client Programm einer verteilten Anwendung muss ein Bindungs Handle erstellen, das der RPC-Laufzeit mitteilt, mit welchem Server eine Verbindung hergestellt werden soll und wie eine Verbindung mit dem Server hergestellt werden soll.

Das folgende Code Fragment veranschaulicht eine gängige Vorgehensweise beim Erstellen eines Bindungs Handles:


```C++
RPC_STATUS status;
unsigned short *StringBinding;
RPC_BINDING_HANDLE BindingHandle;
status = RpcStringBindingCompose(NULL,  // Object UUID
             L"ncacn_ip_tcp",           // Protocol sequence to use
             L"MyServer.MyCompany.com", // Server DNS or Netbios Name
             NULL,
             NULL,
             &StringBinding);
// Error checking ommitted. If no error, we proceed below
status = RpcBindingFromStringBinding(StringBinding, &BindingHandle);

// free string regardless of errors from RpcBindingFromStringBinding
RpcStringFree(&StringBinding);

// Error checking ommitted. If no error, we have a valid binding handle
```



 

 




