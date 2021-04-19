---
description: Signalisiert eine DVD-Fehlerbedingung.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369477"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="6e952-103">EC- \_ DVD- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="6e952-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="6e952-104">Signalisiert eine DVD-Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="6e952-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e952-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e952-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e952-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6e952-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6e952-107">**DWORD** -Wert, der den Fehlerzustand angibt.</span><span class="sxs-lookup"><span data-stu-id="6e952-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="6e952-108">Member des enumerierten Datentyps des [**DVD- \_ Fehlers**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="6e952-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="6e952-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6e952-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6e952-110">Bedeutung hängt vom Wert von *lParam1* ab.</span><span class="sxs-lookup"><span data-stu-id="6e952-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="6e952-111">Weitere Informationen finden Sie unter [**DVD- \_ Fehler**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="6e952-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e952-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e952-112">Remarks</span></span>

<span data-ttu-id="6e952-113">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6e952-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e952-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e952-114">Requirements</span></span>



| <span data-ttu-id="6e952-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e952-115">Requirement</span></span> | <span data-ttu-id="6e952-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6e952-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e952-117">Header</span><span class="sxs-lookup"><span data-stu-id="6e952-117">Header</span></span><br/> | <dl> <span data-ttu-id="6e952-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e952-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e952-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e952-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e952-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6e952-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="6e952-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="6e952-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6e952-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e952-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




