---
title: Erstellen eines Bindungshandpunkts
description: Das Clientprogramm einer verteilten Anwendung muss ein Bindungshand handle erstellen, das die RPC-Laufzeit darüber informiert, welcher Server kontaktiert werden soll und wie der Server kontaktiert werden soll.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- Remoteprozeduraufruf RPC , Aufgaben, Erstellen eines Bindungshandpunkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b1d805a765649f640ff10f8cb825264e3402c8938786d183b0be351036c971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101710"
---
# <a name="creating-a-binding-handle"></a>Erstellen eines Bindungshandpunkts

Das Clientprogramm einer verteilten Anwendung muss ein Bindungshand handle erstellen, das die RPC-Laufzeit darüber informiert, welcher Server kontaktiert werden soll und wie der Server kontaktiert werden soll.

Im folgenden Codefragment wird ein gängiger Ansatz zum Erstellen eines Bindungshandpunkts veranschaulicht:


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



 

 




