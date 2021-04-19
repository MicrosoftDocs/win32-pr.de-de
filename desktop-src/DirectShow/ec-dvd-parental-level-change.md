---
description: Signalisiert, dass die Jugend Stufe des verfassten DVD-Inhalts geändert wird.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360371"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="9cbbd-103">Änderung der EC-DVD-Jugend \_ \_ \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="9cbbd-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="9cbbd-104">Signalisiert, dass die Jugend Stufe des verfassten DVD-Inhalts geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9cbbd-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cbbd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cbbd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbbd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9cbbd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9cbbd-107">Long-Wert, der die neue im Spieler festgelegte Jugend Stufe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9cbbd-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="9cbbd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9cbbd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9cbbd-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="9cbbd-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cbbd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cbbd-110">Remarks</span></span>

<span data-ttu-id="9cbbd-111">Der [DVD-Navigator](dvd-navigator-filter.md) -Filter unterstützt keine Änderungen auf Jugendebene während des Streamings als Reaktion auf settmppml-Befehle auf einem DVD-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="9cbbd-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cbbd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cbbd-112">Requirements</span></span>



| <span data-ttu-id="9cbbd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cbbd-113">Requirement</span></span> | <span data-ttu-id="9cbbd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9cbbd-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbbd-115">Header</span><span class="sxs-lookup"><span data-stu-id="9cbbd-115">Header</span></span><br/> | <dl> <span data-ttu-id="9cbbd-116"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbbd-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbbd-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cbbd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbbd-118">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9cbbd-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="9cbbd-119">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="9cbbd-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9cbbd-120">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9cbbd-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




