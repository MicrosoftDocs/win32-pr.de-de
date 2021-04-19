---
description: Das Diagramm dient zum Verwerfen von Beispielen, um die Qualität zu steuern.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367517"
---
# <a name="ec_quality_change"></a><span data-ttu-id="fc85c-103">EC- \_ Qualitäts \_ Änderung</span><span class="sxs-lookup"><span data-stu-id="fc85c-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="fc85c-104">Das Diagramm dient zum Verwerfen von Beispielen, um die Qualität zu steuern.</span><span class="sxs-lookup"><span data-stu-id="fc85c-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc85c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc85c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc85c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fc85c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fc85c-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="fc85c-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc85c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fc85c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fc85c-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="fc85c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="fc85c-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="fc85c-110">Default Action</span></span>

<span data-ttu-id="fc85c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc85c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc85c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc85c-112">Remarks</span></span>

<span data-ttu-id="fc85c-113">Ein Filter sendet dieses Ereignis, wenn es als Reaktion auf eine Qualitäts Steuerungs Meldung Stichproben löscht.</span><span class="sxs-lookup"><span data-stu-id="fc85c-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="fc85c-114">Das Ereignis wird nur gesendet, wenn es die Qualitätsstufe anpasst, nicht für die einzelnen Abtast.</span><span class="sxs-lookup"><span data-stu-id="fc85c-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="fc85c-115">Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="fc85c-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc85c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc85c-116">Requirements</span></span>



| <span data-ttu-id="fc85c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc85c-117">Requirement</span></span> | <span data-ttu-id="fc85c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fc85c-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc85c-119">Header</span><span class="sxs-lookup"><span data-stu-id="fc85c-119">Header</span></span><br/> | <dl> <span data-ttu-id="fc85c-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc85c-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc85c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc85c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc85c-122">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="fc85c-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fc85c-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc85c-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




