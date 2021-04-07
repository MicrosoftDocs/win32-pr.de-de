---
description: Legt den Schwellenwert fest, bei dem der Encoder ein Video Feld als redundant ansieht.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Avencvideoinverabtelecinethreshold-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745657"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="278cd-103">Avencvideoinverabtelecinethreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="278cd-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="278cd-104">Legt den Schwellenwert fest, bei dem der Encoder ein Video Feld als redundant ansieht.</span><span class="sxs-lookup"><span data-stu-id="278cd-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="278cd-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="278cd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="278cd-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="278cd-106">Data type</span></span>

<span data-ttu-id="278cd-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="278cd-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="278cd-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="278cd-108">Property GUID</span></span>

<span data-ttu-id="278cd-109">**Codecapi \_ avencvideoinverabtelecinethreshold**</span><span class="sxs-lookup"><span data-stu-id="278cd-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="278cd-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="278cd-110">Property value</span></span>

<span data-ttu-id="278cd-111">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="278cd-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="278cd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="278cd-112">Value</span></span> | <span data-ttu-id="278cd-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="278cd-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="278cd-114">0</span><span class="sxs-lookup"><span data-stu-id="278cd-114">0</span></span>     | <span data-ttu-id="278cd-115">Der Encoder ist weniger wahrscheinlich, dass die Videofelder redundant sind.</span><span class="sxs-lookup"><span data-stu-id="278cd-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="278cd-116">100</span><span class="sxs-lookup"><span data-stu-id="278cd-116">100</span></span>   | <span data-ttu-id="278cd-117">Der Encoder ist eher in der Regel redundant, dass die Videofelder redundant sind.</span><span class="sxs-lookup"><span data-stu-id="278cd-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="278cd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="278cd-118">Remarks</span></span>

<span data-ttu-id="278cd-119">Legen Sie diese Eigenschaft fest, wenn der Encoder Inverse Telecine mit einer analogen Videoquelle ausführt.</span><span class="sxs-lookup"><span data-stu-id="278cd-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="278cd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="278cd-120">Requirements</span></span>



| <span data-ttu-id="278cd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="278cd-121">Requirement</span></span> | <span data-ttu-id="278cd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="278cd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="278cd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="278cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="278cd-124">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="278cd-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="278cd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="278cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="278cd-126">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="278cd-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="278cd-127">Header</span><span class="sxs-lookup"><span data-stu-id="278cd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="278cd-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="278cd-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278cd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="278cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278cd-130">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="278cd-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="278cd-131">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="278cd-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




