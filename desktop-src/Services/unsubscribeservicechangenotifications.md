---
description: Abonniert die Dienststatus-Änderungs Benachrichtigungen.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Unabonneatchangenotifications-Funktion (winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866627"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="757d5-103">Unabonneanservicechangenotifications-Funktion</span><span class="sxs-lookup"><span data-stu-id="757d5-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="757d5-104">Abonniert die Dienststatus-Änderungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="757d5-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="757d5-105">Diese Funktion verwendet Abonnements, die von [**abonbeservicechangenotifications**](subscribeservicechangenotifications.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="757d5-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="757d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="757d5-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="757d5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="757d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757d5-108">*pabonnement* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="757d5-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757d5-109">Ein Zeiger auf das Abonnement, das abonniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="757d5-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757d5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="757d5-110">Return value</span></span>

<span data-ttu-id="757d5-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="757d5-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="757d5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="757d5-112">Remarks</span></span>

<span data-ttu-id="757d5-113">Nicht **abonniert beservicechangenotifications** gibt erst zurück, wenn ausstehende Prozess interne Rückrufe beendet sind.</span><span class="sxs-lookup"><span data-stu-id="757d5-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="757d5-114">Daher ist es nicht möglich, nicht **abonniert beservicechangenotifications** innerhalb des Rückrufs aufzurufen, ohne einen Deadlock zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="757d5-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="757d5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="757d5-115">Requirements</span></span>



| <span data-ttu-id="757d5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="757d5-116">Requirement</span></span> | <span data-ttu-id="757d5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="757d5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="757d5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="757d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="757d5-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="757d5-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="757d5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="757d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="757d5-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="757d5-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="757d5-122">Header</span><span class="sxs-lookup"><span data-stu-id="757d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="757d5-123"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="757d5-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="757d5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="757d5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="757d5-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757d5-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757d5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="757d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757d5-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="757d5-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="757d5-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="757d5-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="757d5-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="757d5-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="757d5-130">**Abonniert-servicechangenotifications**</span><span class="sxs-lookup"><span data-stu-id="757d5-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="757d5-131">**Queryservicedynamicinformation**</span><span class="sxs-lookup"><span data-stu-id="757d5-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




