---
description: Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8465825b93207059e5f2ea5f054deb7c3fd5619f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370759"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="1aafc-103">EC \_ errorabortex</span><span class="sxs-lookup"><span data-stu-id="1aafc-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="1aafc-104">Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1aafc-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="1aafc-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aafc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aafc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1aafc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-107">**(HRESULT)** Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1aafc-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="1aafc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1aafc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-109">**(BSTR)** Eine Zeichenfolge, die zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="1aafc-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="1aafc-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="1aafc-110">Default Action</span></span>

<span data-ttu-id="1aafc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1aafc-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aafc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aafc-112">Remarks</span></span>

<span data-ttu-id="1aafc-113">Dieses Ereignis wird vom Legacy- [Windows-Quell](windows-media-source-filter.md) Filter gesendet.</span><span class="sxs-lookup"><span data-stu-id="1aafc-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="1aafc-114">Neue Filter sollten dieses Ereignis nicht senden.</span><span class="sxs-lookup"><span data-stu-id="1aafc-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aafc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aafc-115">Requirements</span></span>



| <span data-ttu-id="1aafc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aafc-116">Requirement</span></span> | <span data-ttu-id="1aafc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1aafc-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aafc-118">Header</span><span class="sxs-lookup"><span data-stu-id="1aafc-118">Header</span></span><br/> | <dl> <span data-ttu-id="1aafc-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aafc-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aafc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aafc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aafc-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="1aafc-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1aafc-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1aafc-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




