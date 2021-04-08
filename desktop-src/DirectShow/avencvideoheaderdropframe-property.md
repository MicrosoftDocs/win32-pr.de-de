---
description: Gibt den Wert des Drop Frame-Flags im Group of Pictures (GOP)-Header an.
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Avencvideoheaderdropframe-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860477"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="7e2d6-103">Avencvideoheaderdropframe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="7e2d6-104">Gibt den Wert des Drop Frame-Flags im Group of Pictures (GOP)-Header an.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="7e2d6-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e2d6-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e2d6-106">Data type</span></span>

<span data-ttu-id="7e2d6-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7e2d6-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="7e2d6-108">Property GUID</span></span>

<span data-ttu-id="7e2d6-109">**Codecapi \_ avencvideoheaderdropframe**</span><span class="sxs-lookup"><span data-stu-id="7e2d6-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="7e2d6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7e2d6-110">Property value</span></span>

<span data-ttu-id="7e2d6-111">Der Wert dieser Eigenschaft kann 0 oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e2d6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e2d6-112">Remarks</span></span>

<span data-ttu-id="7e2d6-113">Der Ablage Frame Modus wird in einem NTSC-Video verwendet, um die Diskrepanz zwischen dem Video, das 29,97 Frames pro Sekunde ist, und der Zeit Code Anzeige (30 Frames pro Sekunde) zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="7e2d6-114">Im Ablage Frame Modus werden die Frame Nummern 00 und 01 am Anfang jeder Minute übersprungen. ausgenommen sind Minuten, bei denen es sich um ein Vielfaches von zehn (00, 10, 20 usw.) handelt.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="7e2d6-115">Nur die Frame Nummern im Zeit Code werden gelöscht. Es werden keine eigentlichen Frames gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2d6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e2d6-116">Requirements</span></span>



| <span data-ttu-id="7e2d6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e2d6-117">Requirement</span></span> | <span data-ttu-id="7e2d6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7e2d6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2d6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2d6-120">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7e2d6-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e2d6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2d6-122">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7e2d6-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7e2d6-123">Header</span><span class="sxs-lookup"><span data-stu-id="7e2d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e2d6-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e2d6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e2d6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e2d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e2d6-126">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="7e2d6-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7e2d6-127">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7e2d6-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




