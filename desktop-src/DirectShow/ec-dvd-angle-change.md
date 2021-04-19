---
description: Signalisiert, dass entweder die Anzahl der verfügbaren Winkel geändert wurde oder die aktuelle Winkel Zahl geändert wurde.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372657"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="a7d86-103">Änderung des EC- \_ DVD- \_ Winkels \_</span><span class="sxs-lookup"><span data-stu-id="a7d86-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="a7d86-104">Signalisiert, dass entweder die Anzahl der verfügbaren Winkel geändert wurde oder die aktuelle Winkel Zahl geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7d86-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7d86-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7d86-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d86-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a7d86-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a7d86-107">**DWORD** -Wert, der die Anzahl der verfügbaren Winkel angibt.</span><span class="sxs-lookup"><span data-stu-id="a7d86-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="a7d86-108">Wenn die Anzahl der verfügbaren Winkel 1 beträgt, ist das aktuelle Video nicht multiangle.</span><span class="sxs-lookup"><span data-stu-id="a7d86-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="a7d86-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a7d86-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a7d86-110">**DWORD** -Wert, der die aktuelle Winkel Zahl angibt.</span><span class="sxs-lookup"><span data-stu-id="a7d86-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7d86-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d86-111">Remarks</span></span>

<span data-ttu-id="a7d86-112">Die Winkel Zahlen reichen von 1 bis 9.</span><span class="sxs-lookup"><span data-stu-id="a7d86-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="a7d86-113">Die aktuelle Spitzen Zahl kann sich automatisch ändern, indem ein Navigations Befehl, der auf der Festplatte erstellt wurde, und die Anwendungssteuerung mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a7d86-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="a7d86-114">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a7d86-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d86-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d86-115">Requirements</span></span>



| <span data-ttu-id="a7d86-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7d86-116">Requirement</span></span> | <span data-ttu-id="a7d86-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d86-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d86-118">Header</span><span class="sxs-lookup"><span data-stu-id="a7d86-118">Header</span></span><br/> | <dl> <span data-ttu-id="a7d86-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d86-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d86-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7d86-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d86-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a7d86-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a7d86-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="a7d86-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a7d86-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a7d86-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




