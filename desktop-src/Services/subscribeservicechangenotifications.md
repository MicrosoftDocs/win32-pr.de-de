---
description: Abonniert Dienststatus-Änderungs Benachrichtigungen mithilfe einer Rückruffunktion.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Abonneanservicechangenotifications-Funktion (winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349599"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="da048-103">Abonniert Service changenotifications-Funktion</span><span class="sxs-lookup"><span data-stu-id="da048-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="da048-104">Abonniert Dienststatus-Änderungs Benachrichtigungen mithilfe einer Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="da048-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="da048-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da048-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="da048-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da048-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da048-107">*hservice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da048-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da048-108">Ein Handle für den Dienst oder ein Handle für den Dienststeuerungs-Manager (SCM), der auf Änderungen überwacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="da048-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="da048-109">Handles für Dienste werden von der [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion und der-Funktion für die Funktion [**"-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " zurückgegeben und müssen über das Zugriffsrecht für **Dienst \_ Abfragen \_** verfügen.</span><span class="sxs-lookup"><span data-stu-id="da048-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="da048-110">Handles für den Dienststeuerungs-Manager werden von der [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion zurückgegeben und müssen das **SC- \_ Manager- \_ \_ Dienst** Zugriffsrecht auflisten.</span><span class="sxs-lookup"><span data-stu-id="da048-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="da048-111">*eeventtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da048-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da048-112">Gibt den Typ der Statusänderungen an, die gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="da048-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="da048-113">Dieser Parameter wird auf einen der Werte festgelegt, die im [**SC- \_ \_ Ereignistyp**](sc-event-type.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="da048-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="da048-114">Das Verhalten dieser Funktion ist abhängig vom Ereignistyp wie folgt unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="da048-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="da048-115">Wert</span><span class="sxs-lookup"><span data-stu-id="da048-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="da048-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="da048-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="da048-117"><dt>**SC \_ \_ \_ Änderung der Ereignis Datenbank**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da048-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="da048-118">Es wurde ein Dienst hinzugefügt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="da048-118">A service has been added or deleted.</span></span> <span data-ttu-id="da048-119">Der *hservice* -Parameter muss ein Handle für den SCM sein.</span><span class="sxs-lookup"><span data-stu-id="da048-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="da048-120"><dt>**SC \_ \_ \_ Änderung der Ereignis Eigenschaft**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="da048-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="da048-121">Mindestens eine Dienst Eigenschaft wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="da048-121">One or more service properties have been updated.</span></span> <span data-ttu-id="da048-122">Der *hservice* -Parameter muss ein Handle für den Dienst sein.</span><span class="sxs-lookup"><span data-stu-id="da048-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="da048-123"><dt>**SC \_ Ereignis \_ Status \_ Änderung**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="da048-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="da048-124">Der Status eines Dienstanbieter hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="da048-124">The status of a service has changed.</span></span> <span data-ttu-id="da048-125">Der *hservice* -Parameter muss ein Handle für den Dienst sein.</span><span class="sxs-lookup"><span data-stu-id="da048-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="da048-126">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da048-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da048-127">Gibt die Rückruffunktion an.</span><span class="sxs-lookup"><span data-stu-id="da048-127">Specifies the callback function.</span></span> <span data-ttu-id="da048-128">Der Rückruf muss als Typ des **SC- \_ Benachrichtigungs \_ Rückrufs** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="da048-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="da048-129">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="da048-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da048-130">*pcallbackcontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="da048-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da048-131">Ein Zeiger, der den Kontext für diesen Benachrichtigungs Rückruf darstellt.</span><span class="sxs-lookup"><span data-stu-id="da048-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="da048-132">*pabonnement* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="da048-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da048-133">Gibt einen Zeiger auf das Abonnement zurück, das sich aus der Benachrichtigungs Rückruf Registrierung ergibt.</span><span class="sxs-lookup"><span data-stu-id="da048-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="da048-134">Der Aufrufer ist für das Aufrufen von [**nicht abonniert beservicechangenotifications**](unsubscribeservicechangenotifications.md) verantwortlich, um den Empfang von Benachrichtigungen zu verhindern</span><span class="sxs-lookup"><span data-stu-id="da048-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da048-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da048-135">Return value</span></span>

<span data-ttu-id="da048-136">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.</span><span class="sxs-lookup"><span data-stu-id="da048-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="da048-137">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der [Systemfehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da048-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="da048-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da048-138">Remarks</span></span>

<span data-ttu-id="da048-139">Die Rückruffunktion wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="da048-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="da048-140">Die Rückruffunktion empfängt einen Zeiger auf den vom Aufrufer bereitgestellten Kontext.</span><span class="sxs-lookup"><span data-stu-id="da048-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="da048-141">Der Rückruf wird als Ergebnis des Dienststatus-Änderungs Ereignisses aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="da048-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="da048-142">Wenn der Rückruf aufgerufen wird, wird er mit einer Bitmaske von \*\*Dienst \_ Benachrichtigen \_ \* xxx\*\*\*-Werten bereitgestellt, die den Typ der Änderung des Dienststatus angeben.</span><span class="sxs-lookup"><span data-stu-id="da048-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="da048-143">Wenn der Rückruf anstelle eines gültigen \*\*\_ diensbenachrichtigungs- \_ \* xxx\*\*\*-Werts mit 0 (null) bereitgestellt wird, muss die Anwendung überprüfen, was geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="da048-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="da048-144">Die Rückruffunktion darf die Ausführung nicht blockieren.</span><span class="sxs-lookup"><span data-stu-id="da048-144">The callback function must not block execution.</span></span> <span data-ttu-id="da048-145">Wenn Sie davon ausgehen, dass die Ausführung der Rückruffunktion Zeit in Anspruch nimmt, sollten Sie die in der Rückruffunktion durchzuführenden Aufgaben in einen separaten Thread auslagern, indem Sie eine Arbeitsaufgabe an einen Thread in einem Thread Pool in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="da048-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="da048-146">Einige Arten von Aufgaben, die die Rückruffunktion in Anspruch nehmen können, sind u. a. das Ausführen von Datei-e/a, das warten auf ein Ereignis und das Ausführen externer Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="da048-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="da048-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da048-147">Requirements</span></span>



| <span data-ttu-id="da048-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da048-148">Requirement</span></span> | <span data-ttu-id="da048-149">Wert</span><span class="sxs-lookup"><span data-stu-id="da048-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da048-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da048-150">Minimum supported client</span></span><br/> | <span data-ttu-id="da048-151">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da048-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="da048-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da048-152">Minimum supported server</span></span><br/> | <span data-ttu-id="da048-153">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da048-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="da048-154">Header</span><span class="sxs-lookup"><span data-stu-id="da048-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="da048-155"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da048-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="da048-156">DLL</span><span class="sxs-lookup"><span data-stu-id="da048-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da048-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da048-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da048-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da048-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da048-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="da048-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="da048-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="da048-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="da048-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="da048-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="da048-162">**Nicht abonniert beservicechangenotifications**</span><span class="sxs-lookup"><span data-stu-id="da048-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="da048-163">**Queryservicedynamicinformation**</span><span class="sxs-lookup"><span data-stu-id="da048-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

