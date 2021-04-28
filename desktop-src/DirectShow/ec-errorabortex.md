---
description: 'EC_ERRORABORTEX: Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.'
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094608"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="0bf64-103">EC \_ ERRORABORTEX</span><span class="sxs-lookup"><span data-stu-id="0bf64-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="0bf64-104">Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0bf64-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="0bf64-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf64-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf64-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0bf64-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0bf64-107">**(HRESULT)** Fehlercode des fehlgeschlagenen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0bf64-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="0bf64-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0bf64-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0bf64-109">**(BSTR)** Zeichenfolge, die zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="0bf64-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0bf64-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="0bf64-110">Default Action</span></span>

<span data-ttu-id="0bf64-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0bf64-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf64-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bf64-112">Remarks</span></span>

<span data-ttu-id="0bf64-113">Der ältere [Windows Media Source-Filter](windows-media-source-filter.md) sendet dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0bf64-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="0bf64-114">Neue Filter sollten dieses Ereignis nicht senden.</span><span class="sxs-lookup"><span data-stu-id="0bf64-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf64-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf64-115">Requirements</span></span>



| <span data-ttu-id="0bf64-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf64-116">Requirement</span></span> | <span data-ttu-id="0bf64-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0bf64-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf64-118">Header</span><span class="sxs-lookup"><span data-stu-id="0bf64-118">Header</span></span><br/> | <dl> <span data-ttu-id="0bf64-119"><dt>Dshow.h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf64-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf64-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0bf64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf64-121">Ereignisbenachrichtigungscodes</span><span class="sxs-lookup"><span data-stu-id="0bf64-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0bf64-122">Ereignisbenachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0bf64-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




