---
description: Gibt an, wie weit hinter dem Zeitplan eine Komponente für die Verarbeitung von Beispielen liegt.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357313"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="80087-103">Wartezeit für EC- \_ Beispiel \_</span><span class="sxs-lookup"><span data-stu-id="80087-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="80087-104">Gibt an, wie weit hinter dem Zeitplan eine Komponente für die Verarbeitung von Beispielen liegt.</span><span class="sxs-lookup"><span data-stu-id="80087-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="80087-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="80087-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80087-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="80087-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="80087-107">(Konstante **Referenz \_ Zeit** \* ), die sich hinter der Komponente befindet, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="80087-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="80087-108">Wenn dieser Wert positiv ist, befindet sich die Komponente hinter dem Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="80087-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="80087-109">Wenn dieser Wert negativ ist, liegt die Komponente vor dem Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="80087-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="80087-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="80087-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="80087-111">Keinen.</span><span class="sxs-lookup"><span data-stu-id="80087-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="80087-112">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="80087-112">Default Action</span></span>

<span data-ttu-id="80087-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="80087-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="80087-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80087-114">Remarks</span></span>

<span data-ttu-id="80087-115">Ein benutzerdefinierter Presenter für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR) kann diese Nachricht an den EVR senden, um den EVR zu benachrichtigen, ob der Presenter hinter einem Zeitplan oder vor dem Zeitplan steht.</span><span class="sxs-lookup"><span data-stu-id="80087-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="80087-116">Die einfachste Möglichkeit zum Berechnen *von lParam1* ist: *QPC now*   *QPC Target*, wobei *QPC jetzt* die Uhrzeit und *QPC Target* die Präsentationszeit ist.</span><span class="sxs-lookup"><span data-stu-id="80087-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="80087-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80087-117">Requirements</span></span>



| <span data-ttu-id="80087-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80087-118">Requirement</span></span> | <span data-ttu-id="80087-119">Wert</span><span class="sxs-lookup"><span data-stu-id="80087-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80087-120">Header</span><span class="sxs-lookup"><span data-stu-id="80087-120">Header</span></span><br/> | <dl> <span data-ttu-id="80087-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="80087-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80087-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80087-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80087-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="80087-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="80087-124">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="80087-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

