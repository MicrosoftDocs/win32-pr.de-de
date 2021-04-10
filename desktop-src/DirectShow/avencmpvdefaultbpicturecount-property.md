---
description: Gibt die Standard Anzahl von aufeinander folgenden B-Frames zwischen I-und P-Frames an.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Avencmpvdefaultbpicturecount-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041269"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="4bd72-103">Avencmpvdefaultbpicturecount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bd72-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="4bd72-104">Gibt die Standard Anzahl von aufeinander folgenden B-Frames zwischen I-und P-Frames an.</span><span class="sxs-lookup"><span data-stu-id="4bd72-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="4bd72-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4bd72-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4bd72-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4bd72-106">Data type</span></span>

<span data-ttu-id="4bd72-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4bd72-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4bd72-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="4bd72-108">Property GUID</span></span>

<span data-ttu-id="4bd72-109">**Codecapi \_ avencmpvdefaultbpicturecount**</span><span class="sxs-lookup"><span data-stu-id="4bd72-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="4bd72-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4bd72-110">Property value</span></span>

<span data-ttu-id="4bd72-111">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="4bd72-111">This property has a linear range of values.</span></span> <span data-ttu-id="4bd72-112">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="4bd72-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd72-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bd72-113">Remarks</span></span>

<span data-ttu-id="4bd72-114">Vor Windows 8 gilt diese Eigenschaft für MPEG-Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="4bd72-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="4bd72-115">Ab Windows 8 wird diese Eigenschaft von MPEG-, WMV-und H. 264-Video Encodern verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bd72-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="4bd72-116">Wenn der Encoder diese Eigenschaft unterstützt, kann er zum Steuern der GOP-Struktur (Group of Pictures) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd72-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd72-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bd72-117">Requirements</span></span>



| <span data-ttu-id="4bd72-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bd72-118">Requirement</span></span> | <span data-ttu-id="4bd72-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4bd72-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd72-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bd72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd72-121">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd72-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4bd72-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bd72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd72-123">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4bd72-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4bd72-124">Header</span><span class="sxs-lookup"><span data-stu-id="4bd72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd72-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd72-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd72-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bd72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd72-127">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="4bd72-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4bd72-128">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4bd72-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




