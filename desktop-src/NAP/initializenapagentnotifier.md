---
title: Initializenapagentnotifier-Funktion (naputil. h)
description: Abonniert den aufrufenden Prozess zum Anzeigen von NAPAgent-Status Änderungs Benachrichtigungen und zum Quarantäne Status Änderungs Benachrichtigungen.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Initializenapagentnotifier-Funktion NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949661"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="e3820-104">Initializenapagentnotifier-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3820-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="e3820-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3820-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e3820-106">Die **initializenapagentnotifier** -Funktion abonniert den aufrufenden Prozess zum Anzeigen von NAPAgent-Status Änderungs Benachrichtigungen und zum Quarantäne Status Änderungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e3820-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="e3820-107">Diese Benachrichtigungen werden vom NAPAgent-Dienst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e3820-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3820-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3820-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="e3820-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3820-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3820-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3820-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3820-111">Ein [**napnotifytype**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) -Wert, der den Typ der zu empfangenden Dienst Benachrichtigungen angibt.</span><span class="sxs-lookup"><span data-stu-id="e3820-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="e3820-112">*hnotischyevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3820-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3820-113">Ein Ereignis handle, das für die Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3820-113">An event handle used for notification.</span></span> <span data-ttu-id="e3820-114">Der Aufrufer muss ein geöffnetes Handle an den *hnotifyevent* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e3820-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="e3820-115">Der Aufrufer muss auch das Ereignis handle schließen, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e3820-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3820-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3820-116">Return value</span></span>



| <span data-ttu-id="e3820-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e3820-117">Return code</span></span>                                                                                                | <span data-ttu-id="e3820-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3820-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3820-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e3820-120">Die Initialisierung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e3820-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e3820-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="e3820-122">Fehler bei der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="e3820-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="e3820-123"><dt>**Fehler \_ bereits \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e3820-124">Der Prozess hat die NAPAgent-Dienst Benachrichtigungen vom angegebenen *Typ* bereits abonniert.</span><span class="sxs-lookup"><span data-stu-id="e3820-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="e3820-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="e3820-126">Ein ungültiges Argument wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="e3820-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e3820-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3820-127">Remarks</span></span>

<span data-ttu-id="e3820-128">Diese Funktion ist nicht threadsicher.</span><span class="sxs-lookup"><span data-stu-id="e3820-128">This function is not thread safe.</span></span>

<span data-ttu-id="e3820-129">Bei jedem Prozess, bei dem ein Abonnement für die NAPAgent-Dienst Benachrichtigungen vom angegebenen *Typ* erforderlich ist, muss **initializenapagentnotifier** aufgerufen werden, um Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="e3820-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="e3820-130">Wenn ein Prozess mehr als einen Benachrichtigungstyp abonnieren muss, muss er für jeden Benachrichtigungstyp einmal **initializenapagentnotifier** aufruft.</span><span class="sxs-lookup"><span data-stu-id="e3820-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="e3820-131">Wenn ein Prozess keine weiteren Benachrichtigungen erfordert, muss der Prozess [**uninitializenapagentnotifier**](uninitializenapagentnotifier.md) für den angegebenen *Typ* aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3820-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3820-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3820-132">Requirements</span></span>



| <span data-ttu-id="e3820-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3820-133">Requirement</span></span> | <span data-ttu-id="e3820-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e3820-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3820-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3820-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3820-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3820-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e3820-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3820-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3820-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3820-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e3820-139">Header</span><span class="sxs-lookup"><span data-stu-id="e3820-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3820-140"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="e3820-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e3820-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3820-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3820-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3820-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3820-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3820-144">**Uninitializenapagentnotifier**</span><span class="sxs-lookup"><span data-stu-id="e3820-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





