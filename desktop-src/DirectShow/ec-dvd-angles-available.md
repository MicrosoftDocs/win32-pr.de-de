---
description: Gibt an, ob ein Winkel Block wiedergegeben und Winkel Änderungen durchgeführt werden können.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373914"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="42659-103">EC- \_ DVD- \_ Winkel \_ verfügbar</span><span class="sxs-lookup"><span data-stu-id="42659-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="42659-104">Gibt an, ob ein Winkel Block wiedergegeben und Winkel Änderungen durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="42659-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="42659-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="42659-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42659-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="42659-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="42659-107">Boolescher Wert (**boolescher** Wert), der angibt, ob ein Winkel Block wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42659-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="42659-108">NULL (0) gibt an, dass die Wiedergabe nicht in einem Winkel Block vorhanden ist und keine Winkel verfügbar sind, eins (1) gibt an, dass ein Winkel Block wiedergegeben wird und Winkel Änderungen durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="42659-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="42659-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="42659-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="42659-110">Keinen.</span><span class="sxs-lookup"><span data-stu-id="42659-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42659-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42659-111">Remarks</span></span>

<span data-ttu-id="42659-112">Winkel Änderungen sind nicht auf Winkel Blöcke beschränkt, und die Darstellung der Winkel Änderung kann nur in einem Winkel Block angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42659-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="42659-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42659-113">Requirements</span></span>



| <span data-ttu-id="42659-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42659-114">Requirement</span></span> | <span data-ttu-id="42659-115">Wert</span><span class="sxs-lookup"><span data-stu-id="42659-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42659-116">Header</span><span class="sxs-lookup"><span data-stu-id="42659-116">Header</span></span><br/> | <dl> <span data-ttu-id="42659-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42659-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42659-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42659-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42659-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="42659-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="42659-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="42659-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="42659-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="42659-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




