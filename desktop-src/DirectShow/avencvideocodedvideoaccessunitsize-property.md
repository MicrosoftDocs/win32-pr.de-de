---
description: Gibt die Größe der Video Zugriffs Einheiten in Bytes an. Diese Eigenschaft gilt nur für die Steuermodi der Variablen Bitrate (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Avencvideocodedvideoaccessunitsize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957732"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="5c60a-104">Avencvideocodedvideoaccessunitsize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5c60a-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="5c60a-105">Gibt die Größe der Video Zugriffs Einheiten in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="5c60a-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="5c60a-106">Diese Eigenschaft gilt nur für die Steuermodi der Variablen Bitrate (VBR).</span><span class="sxs-lookup"><span data-stu-id="5c60a-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="5c60a-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5c60a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c60a-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5c60a-108">Data type</span></span>

<span data-ttu-id="5c60a-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="5c60a-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5c60a-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="5c60a-110">Property GUID</span></span>

<span data-ttu-id="5c60a-111">**Codecapi \_ avencvideocodedvideoaccessunitsize**</span><span class="sxs-lookup"><span data-stu-id="5c60a-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="5c60a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5c60a-112">Property value</span></span>

<span data-ttu-id="5c60a-113">Diese Eigenschaft wird als Wertebereich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c60a-113">This property is returned as a range of values.</span></span> <span data-ttu-id="5c60a-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="5c60a-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c60a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c60a-115">Requirements</span></span>



| <span data-ttu-id="5c60a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c60a-116">Requirement</span></span> | <span data-ttu-id="5c60a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5c60a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c60a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c60a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5c60a-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5c60a-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5c60a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c60a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5c60a-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5c60a-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5c60a-122">Header</span><span class="sxs-lookup"><span data-stu-id="5c60a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c60a-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c60a-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c60a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c60a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c60a-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="5c60a-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5c60a-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5c60a-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




