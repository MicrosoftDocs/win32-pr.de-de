---
description: Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863983"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="20d30-103">Mfpkey- \_ videosc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20d30-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="20d30-104">Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="20d30-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="20d30-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="20d30-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="20d30-106">g \_ wszwmvcvideosc.</span><span class="sxs-lookup"><span data-stu-id="20d30-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="20d30-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="20d30-107">Data Type</span></span>

<span data-ttu-id="20d30-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="20d30-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="20d30-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="20d30-109">Default Value</span></span>

<span data-ttu-id="20d30-110">0</span><span class="sxs-lookup"><span data-stu-id="20d30-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="20d30-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20d30-111">Remarks</span></span>

<span data-ttu-id="20d30-112">Die Video Skalierung ist eine Art von perzeptueller Optimierung, die die visuelle Qualität von Videos verbessert, die zu niedrigen Bitraten codiert sind.</span><span class="sxs-lookup"><span data-stu-id="20d30-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="20d30-113">Die Video Skalierungs Optimierung reduziert ausgeprägte Artefakte, kann aber auch Bilddetails Opfern.</span><span class="sxs-lookup"><span data-stu-id="20d30-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="20d30-114">Diese Optimierung wirkt sich auf den Luma-Bereich des codierten Videos aus, wie unten beschrieben, wirkt sich jedoch nicht auf die physische Auflösung des Ausgabevideos aus.</span><span class="sxs-lookup"><span data-stu-id="20d30-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="20d30-115">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="20d30-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="20d30-116">Wert</span><span class="sxs-lookup"><span data-stu-id="20d30-116">Value</span></span> | <span data-ttu-id="20d30-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20d30-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d30-118">0</span><span class="sxs-lookup"><span data-stu-id="20d30-118">0</span></span>     | <span data-ttu-id="20d30-119">Die Video Skalierung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="20d30-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="20d30-120">1</span><span class="sxs-lookup"><span data-stu-id="20d30-120">1</span></span>     | <span data-ttu-id="20d30-121">Der Encoder verwendet die konservative Video Skalierungs Optimierung.</span><span class="sxs-lookup"><span data-stu-id="20d30-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="20d30-122">Der Bereich "Luma" wird von 0... 255 auf 26... 229 skaliert.</span><span class="sxs-lookup"><span data-stu-id="20d30-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="20d30-123">2</span><span class="sxs-lookup"><span data-stu-id="20d30-123">2</span></span>     | <span data-ttu-id="20d30-124">Der Encoder verwendet die aggressive Optimierung der Video Skalierung.</span><span class="sxs-lookup"><span data-stu-id="20d30-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="20d30-125">Der Bereich "Luma" wird von 0... 255 bis 31... 224 skaliert.</span><span class="sxs-lookup"><span data-stu-id="20d30-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="20d30-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20d30-126">Requirements</span></span>



| <span data-ttu-id="20d30-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20d30-127">Requirement</span></span> | <span data-ttu-id="20d30-128">Wert</span><span class="sxs-lookup"><span data-stu-id="20d30-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20d30-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20d30-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20d30-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20d30-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="20d30-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20d30-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20d30-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20d30-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20d30-133">Header</span><span class="sxs-lookup"><span data-stu-id="20d30-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="20d30-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="20d30-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d30-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20d30-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d30-136">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20d30-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




