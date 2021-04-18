---
description: Gibt den Zeitstempel für den letzten Frame Schritt an.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361306"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="39bbc-103">\_Zeit für \_ Zeit Bereinigung</span><span class="sxs-lookup"><span data-stu-id="39bbc-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="39bbc-104">Gibt den Zeitstempel für den letzten Frame Schritt an.</span><span class="sxs-lookup"><span data-stu-id="39bbc-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="39bbc-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="39bbc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bbc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="39bbc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="39bbc-107">(**DWORD**) Niedrigere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="39bbc-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="39bbc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="39bbc-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="39bbc-109">(**DWORD**) Obere 32 Bits des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="39bbc-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="39bbc-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="39bbc-110">Default Action</span></span>

<span data-ttu-id="39bbc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="39bbc-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bbc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39bbc-112">Remarks</span></span>

<span data-ttu-id="39bbc-113">Der Präsentator für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR) sendet diese Nachricht an den EVR, wenn er einen Frame Schritt abschließt.</span><span class="sxs-lookup"><span data-stu-id="39bbc-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bbc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39bbc-114">Requirements</span></span>



| <span data-ttu-id="39bbc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39bbc-115">Requirement</span></span> | <span data-ttu-id="39bbc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="39bbc-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39bbc-117">Header</span><span class="sxs-lookup"><span data-stu-id="39bbc-117">Header</span></span><br/> | <dl> <span data-ttu-id="39bbc-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bbc-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39bbc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39bbc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bbc-120">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="39bbc-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




