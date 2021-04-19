---
description: Wird vom WM-ASF-Writer-Filter gesendet, wenn die Vorverarbeitung für Multipass-Codierung abgeschlossen ist.
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: EC_PREPROCESS_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367518"
---
# <a name="ec_preprocess_complete"></a><span data-ttu-id="97104-103">EC- \_ Vorverarbeitung ist \_ beendet</span><span class="sxs-lookup"><span data-stu-id="97104-103">EC\_PREPROCESS\_COMPLETE</span></span>

<span data-ttu-id="97104-104">Wird vom [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter gesendet, wenn die Vorverarbeitung für Multipass-Codierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="97104-104">Sent by the [WM ASF Writer](wm-asf-writer-filter.md) filter when it completes the pre-processing for multipass encoding.</span></span>

## <a name="parameters"></a><span data-ttu-id="97104-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="97104-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97104-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="97104-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="97104-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="97104-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="97104-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="97104-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="97104-109">(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters.</span><span class="sxs-lookup"><span data-stu-id="97104-109">(**IUnknown**\*) Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="97104-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="97104-110">Default Action</span></span>

<span data-ttu-id="97104-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="97104-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="97104-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97104-112">Requirements</span></span>



| <span data-ttu-id="97104-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97104-113">Requirement</span></span> | <span data-ttu-id="97104-114">Wert</span><span class="sxs-lookup"><span data-stu-id="97104-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97104-115">Header</span><span class="sxs-lookup"><span data-stu-id="97104-115">Header</span></span><br/> | <dl> <span data-ttu-id="97104-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="97104-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97104-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97104-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97104-118">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="97104-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="97104-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="97104-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




