---
description: Event Handler Prototype-Funktionen werden für alle Funktionen verwendet, die Winlogon-Benachrichtigungsereignisse behandeln.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Rückruffunktion "Prototyp" der Ereignishandlerfunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: df6670e852ccd12fd2bed1d0c188aa0252c9b3afbcb899cf9480b7011d08625d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008228"
---
# <a name="event-handler-function-prototype-callback-function"></a>Rückruffunktion "Prototyp" der Ereignishandlerfunktion

\[Funktionen des Ereignishandlerprototyps können ab Windows Server 2008 und Windows Vista nicht mehr verwendet werden. \]

Ereignishandler-Prototypfunktionen werden für alle Funktionen verwendet, die [*Winlogon-Benachrichtigungsereignisse*](/windows/desktop/SecGloss/w-gly) behandeln. Der Name der Funktion, der unten durch den Platzhalter *Event \_ Handler Function \_ \_ Name* dargestellt wird, spiegelt in der Regel den Namen des Ereignisses wider, das von der Funktion behandelt wird. Beispielsweise könnte die Funktion, die Anmeldeereignisse behandelt, den Namen **WLEventLogon haben.**

## <a name="syntax"></a>Syntax


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**WLX \_ NOTIFICATION \_ INFO-Struktur,**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) die die Details des Ereignisses enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Ihr Ereignishandler untergeordnete Prozesse erstellen muss, sollte er die [**CreateProcessAsUser-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) aufrufen. Andernfalls wird der neue Prozess auf dem Winlogon-Desktop und nicht auf dem Desktop des Benutzers erstellt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Ereignishandler für Winlogon-Ereignisse implementiert werden. Der Einfachheit halber werden nur die Implementierungen der Logon- und Logoff-Ereignishandler angezeigt. Sie können Handler für die restlichen Ereignisse genau auf die gleiche Weise implementieren.


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

