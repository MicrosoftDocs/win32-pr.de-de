---
description: Gibt das Energiespar Niveau eines Video-Decoders an.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Avdecvideoswpowerlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339666"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="312ac-103">Avdecvideoswpowerlevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="312ac-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="312ac-104">Gibt das Energiespar Niveau eines Video-Decoders an.</span><span class="sxs-lookup"><span data-stu-id="312ac-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="312ac-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="312ac-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="312ac-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="312ac-106">Data type</span></span>

<span data-ttu-id="312ac-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="312ac-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="312ac-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="312ac-108">Property GUID</span></span>

<span data-ttu-id="312ac-109">**Codecapi \_ avdecvideoswpowerlevel**</span><span class="sxs-lookup"><span data-stu-id="312ac-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="312ac-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="312ac-110">Property value</span></span>

<span data-ttu-id="312ac-111">Der Bereich möglicher Werte ist \[ 0.. 100 \] , einschließlich der folgenden Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="312ac-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="312ac-112">Wert</span><span class="sxs-lookup"><span data-stu-id="312ac-112">Value</span></span> | <span data-ttu-id="312ac-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="312ac-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="312ac-114">0</span><span class="sxs-lookup"><span data-stu-id="312ac-114">0</span></span>     | <span data-ttu-id="312ac-115">Optimieren Sie die Akku Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="312ac-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="312ac-116">100</span><span class="sxs-lookup"><span data-stu-id="312ac-116">100</span></span>   | <span data-ttu-id="312ac-117">Optimieren Sie die Videoqualität.</span><span class="sxs-lookup"><span data-stu-id="312ac-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="312ac-118">Die [**eavdecvideoswpowerlevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) -Enumeration definiert einige bestimmte Konstanten innerhalb dieses Bereichs.</span><span class="sxs-lookup"><span data-stu-id="312ac-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="312ac-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="312ac-119">Remarks</span></span>

<span data-ttu-id="312ac-120">Sie können diese Eigenschaft während der Wiedergabe festlegen, um die Energiespar Stufe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="312ac-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="312ac-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="312ac-121">Requirements</span></span>



| <span data-ttu-id="312ac-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="312ac-122">Requirement</span></span> | <span data-ttu-id="312ac-123">Wert</span><span class="sxs-lookup"><span data-stu-id="312ac-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="312ac-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="312ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="312ac-125">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="312ac-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="312ac-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="312ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="312ac-127">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="312ac-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="312ac-128">Header</span><span class="sxs-lookup"><span data-stu-id="312ac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="312ac-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="312ac-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="312ac-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="312ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312ac-131">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="312ac-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="312ac-132">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="312ac-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




