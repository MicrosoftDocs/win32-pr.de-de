---
description: Signalisiert eine DVD-Warnungs Bedingung.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373657"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="2a902-103">EC- \_ DVD- \_ Warnung</span><span class="sxs-lookup"><span data-stu-id="2a902-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="2a902-104">Signalisiert eine DVD-Warnungs Bedingung.</span><span class="sxs-lookup"><span data-stu-id="2a902-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a902-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a902-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a902-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2a902-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2a902-107">**DWORD** -Wert, der die Warnungs Bedingung angibt.</span><span class="sxs-lookup"><span data-stu-id="2a902-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="2a902-108">Member des enumerierten Datentyps der [**DVD- \_ Warnung**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .</span><span class="sxs-lookup"><span data-stu-id="2a902-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="2a902-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2a902-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2a902-110">Wenn *pParam1* den Wert "DVD \_ Warning \_ Open", "DVD \_ Warning Seek" oder " \_ DVD \_ Warning Read" \_ aufweist, enthält *lParam2* den letzten von " **GetLastError**" zurückgegebenen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2a902-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a902-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a902-111">Requirements</span></span>



| <span data-ttu-id="2a902-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a902-112">Requirement</span></span> | <span data-ttu-id="2a902-113">Wert</span><span class="sxs-lookup"><span data-stu-id="2a902-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a902-114">Header</span><span class="sxs-lookup"><span data-stu-id="2a902-114">Header</span></span><br/> | <dl> <span data-ttu-id="2a902-115"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a902-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a902-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a902-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a902-117">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2a902-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2a902-118">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="2a902-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2a902-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a902-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




