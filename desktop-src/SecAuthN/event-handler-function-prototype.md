---
description: Die Prototypfunktionen von Ereignis Handlern werden für alle Funktionen verwendet, die Winlogon-Benachrichtigungs Ereignisse verarbeiten.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Rückruffunktion der Ereignis Handler-Funktion
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
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364187"
---
# <a name="event-handler-function-prototype-callback-function"></a>Rückruffunktion der Ereignis Handler-Funktion

\[Funktionen des ereignishandlerprototyps sind nicht mehr zur Verwendung ab Windows Server 2008 und Windows Vista verfügbar. \]

Die Prototypfunktionen von Ereignis Handlern werden für alle Funktionen verwendet, die [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Benachrichtigungs Ereignisse verarbeiten. Der Name der Funktion, die unten durch den *\_ \_ Funktions \_ Namen* des Platzhalter-Ereignis Handlers dargestellt wird, gibt in der Regel den Namen des Ereignisses wieder, das von der Funktion verarbeitet wird. Beispielsweise könnte die Funktion, die die Anmelde Ereignisse behandelt, den Namen " **WLEventLogon**" haben.

## <a name="syntax"></a>Syntax


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**wlx- \_ Benachrichtigungs \_ Informations**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) Struktur, die die Details des Ereignisses enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Ihr Ereignishandler untergeordnete Prozesse erstellen muss, sollte [**er die Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) "-Funktion" aufrufen. Andernfalls wird der neue Prozess auf dem Winlogon-Desktop erstellt, nicht auf dem Desktop des Benutzers.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Ereignishandler für Winlogon-Ereignisse implementiert werden. Der Einfachheit halber werden nur die Implementierungen der Anmelde-und Abmelde Ereignishandler angezeigt. Sie können Handler für die restlichen Ereignisse auf genau die gleiche Weise implementieren.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

