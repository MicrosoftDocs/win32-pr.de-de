---
description: Gibt die Anzahl der Video Frames zurück, die der Encoder empfangen hat.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Avencstatus videototalframes-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345584"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="915c1-103">Avencstatus videototalframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="915c1-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="915c1-104">Gibt die Anzahl der Video Frames zurück, die der Encoder empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="915c1-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="915c1-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="915c1-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="915c1-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="915c1-106">Data type</span></span>

<span data-ttu-id="915c1-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="915c1-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="915c1-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="915c1-108">Property GUID</span></span>

<span data-ttu-id="915c1-109">**Codecapi \_ avencstatus Video Total Frames**</span><span class="sxs-lookup"><span data-stu-id="915c1-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="915c1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="915c1-110">Remarks</span></span>

<span data-ttu-id="915c1-111">Diese Eigenschaft ist nach Abschluss der Codierung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="915c1-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="915c1-112">Der Wert dieser Eigenschaft ist die Gesamtzahl der an den Encoder gesendeten Frames, einschließlich abgelöschter Frames.</span><span class="sxs-lookup"><span data-stu-id="915c1-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="915c1-113">Um die Anzahl der codierten Frames zu erhalten, lesen Sie die Eigenschaft " [**avencstatus videocodedframes**](avencstatvideocodedframes-property.md) ".</span><span class="sxs-lookup"><span data-stu-id="915c1-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="915c1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="915c1-114">Requirements</span></span>



| <span data-ttu-id="915c1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="915c1-115">Requirement</span></span> | <span data-ttu-id="915c1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="915c1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="915c1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="915c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="915c1-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="915c1-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="915c1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="915c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="915c1-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="915c1-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="915c1-121">Header</span><span class="sxs-lookup"><span data-stu-id="915c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="915c1-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="915c1-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915c1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="915c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915c1-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="915c1-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="915c1-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="915c1-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




