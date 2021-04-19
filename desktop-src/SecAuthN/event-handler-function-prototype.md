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
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="a3bf6-103">Rückruffunktion der Ereignis Handler-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3bf6-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="a3bf6-104">\[Funktionen des ereignishandlerprototyps sind nicht mehr zur Verwendung ab Windows Server 2008 und Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a3bf6-105">\]</span><span class="sxs-lookup"><span data-stu-id="a3bf6-105">\]</span></span>

<span data-ttu-id="a3bf6-106">Die Prototypfunktionen von Ereignis Handlern werden für alle Funktionen verwendet, die [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Benachrichtigungs Ereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="a3bf6-107">Der Name der Funktion, die unten durch den *\_ \_ Funktions \_ Namen* des Platzhalter-Ereignis Handlers dargestellt wird, gibt in der Regel den Namen des Ereignisses wieder, das von der Funktion verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="a3bf6-108">Beispielsweise könnte die Funktion, die die Anmelde Ereignisse behandelt, den Namen " **WLEventLogon**" haben.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bf6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3bf6-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a3bf6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3bf6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bf6-111">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3bf6-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bf6-112">Ein Zeiger auf eine [**wlx- \_ Benachrichtigungs \_ Informations**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) Struktur, die die Details des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3bf6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3bf6-113">Return value</span></span>

<span data-ttu-id="a3bf6-114">Diese Rückruffunktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3bf6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3bf6-115">Remarks</span></span>

<span data-ttu-id="a3bf6-116">Wenn Ihr Ereignishandler untergeordnete Prozesse erstellen muss, sollte [**er die Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) "-Funktion" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="a3bf6-117">Andernfalls wird der neue Prozess auf dem Winlogon-Desktop erstellt, nicht auf dem Desktop des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="a3bf6-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3bf6-118">Examples</span></span>

<span data-ttu-id="a3bf6-119">Im folgenden Beispiel wird gezeigt, wie Ereignishandler für Winlogon-Ereignisse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="a3bf6-120">Der Einfachheit halber werden nur die Implementierungen der Anmelde-und Abmelde Ereignishandler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="a3bf6-121">Sie können Handler für die restlichen Ereignisse auf genau die gleiche Weise implementieren.</span><span class="sxs-lookup"><span data-stu-id="a3bf6-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a3bf6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3bf6-122">Requirements</span></span>



| <span data-ttu-id="a3bf6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3bf6-123">Requirement</span></span> | <span data-ttu-id="a3bf6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a3bf6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3bf6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3bf6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a3bf6-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3bf6-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a3bf6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3bf6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a3bf6-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3bf6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a3bf6-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a3bf6-129">End of client support</span></span><br/>    | <span data-ttu-id="a3bf6-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3bf6-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a3bf6-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a3bf6-131">End of server support</span></span><br/>    | <span data-ttu-id="a3bf6-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3bf6-132">Windows Server 2003</span></span><br/>                       |



 

