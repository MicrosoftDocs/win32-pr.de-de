---
description: Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt. Diese Eigenschaft gilt für MPEG-Video Encoder.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Avencmpvgopopen-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746928"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="0b075-104">Avencmpvgopopen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b075-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="0b075-105">Gibt an, ob der Encoder offene Gruppen von Bildern (GOPs) oder geschlossene GOPs erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0b075-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="0b075-106">Diese Eigenschaft gilt für MPEG-Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="0b075-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="0b075-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0b075-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b075-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0b075-108">Data type</span></span>

<span data-ttu-id="0b075-109">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="0b075-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0b075-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="0b075-110">Property GUID</span></span>

<span data-ttu-id="0b075-111">**Codecapi \_ avencmpvgopopen**</span><span class="sxs-lookup"><span data-stu-id="0b075-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="0b075-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0b075-112">Property value</span></span>



| <span data-ttu-id="0b075-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0b075-113">Value</span></span>          | <span data-ttu-id="0b075-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b075-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="0b075-115">Variant \_ false</span><span class="sxs-lookup"><span data-stu-id="0b075-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="0b075-116">Geschlossene GOPs</span><span class="sxs-lookup"><span data-stu-id="0b075-116">Closed GOPs</span></span> |
| <span data-ttu-id="0b075-117">Variant \_ true</span><span class="sxs-lookup"><span data-stu-id="0b075-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="0b075-118">Open-GOPs</span><span class="sxs-lookup"><span data-stu-id="0b075-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="0b075-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b075-119">Remarks</span></span>

<span data-ttu-id="0b075-120">Ein geöffnetes GOP enthält Delta Frames, die auf Frames aus dem vorherigen GOP verweisen.</span><span class="sxs-lookup"><span data-stu-id="0b075-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="0b075-121">Ein geschlossenes GOP enthält keine Delta Frames, die auf das vorherige GOP verweisen.</span><span class="sxs-lookup"><span data-stu-id="0b075-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b075-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b075-122">Requirements</span></span>



| <span data-ttu-id="0b075-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b075-123">Requirement</span></span> | <span data-ttu-id="0b075-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0b075-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b075-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b075-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b075-126">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0b075-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0b075-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b075-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b075-128">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0b075-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0b075-129">Header</span><span class="sxs-lookup"><span data-stu-id="0b075-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b075-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b075-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b075-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b075-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b075-132">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="0b075-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0b075-133">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0b075-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




