---
description: Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348319"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="7be75-103">Mfpkey- \_ decodercomplexityangeforderten-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7be75-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="7be75-104">Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="7be75-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="7be75-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7be75-105">Data Type</span></span>

<span data-ttu-id="7be75-106">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7be75-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7be75-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="7be75-107">Default Value</span></span>

<span data-ttu-id="7be75-108">1</span><span class="sxs-lookup"><span data-stu-id="7be75-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7be75-109">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7be75-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="7be75-110">g \_ wszwmvcdecodercomplexityangefordert</span><span class="sxs-lookup"><span data-stu-id="7be75-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="7be75-111">Datentyp für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7be75-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="7be75-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7be75-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="7be75-113">Standardwert für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7be75-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="7be75-114">Schlanken</span><span class="sxs-lookup"><span data-stu-id="7be75-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="7be75-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7be75-115">Remarks</span></span>

<span data-ttu-id="7be75-116">Der Codec versucht, den Inhalt mithilfe der Geräte Konformitäts Vorlage zu codieren, die durch diesen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7be75-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="7be75-117">Die tatsächliche Vorlage, der der codierte Inhalt entspricht, kann nach der Codierung von der [mfpkey- \_ decodercomplexityprofile](mfpkey-decodercomplexityprofileproperty.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7be75-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="7be75-118">Diese Eigenschaft muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7be75-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="7be75-119">Wert für IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="7be75-119">Value for IPropertyStore</span></span> | <span data-ttu-id="7be75-120">Wert für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7be75-120">Value for IPropertyBag</span></span> | <span data-ttu-id="7be75-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7be75-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="7be75-122">0</span><span class="sxs-lookup"><span data-stu-id="7be75-122">0</span></span>                        | <span data-ttu-id="7be75-123">El</span><span class="sxs-lookup"><span data-stu-id="7be75-123">"SP"</span></span>                   | <span data-ttu-id="7be75-124">einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="7be75-124">simple profile</span></span>      |
| <span data-ttu-id="7be75-125">1</span><span class="sxs-lookup"><span data-stu-id="7be75-125">1</span></span>                        | <span data-ttu-id="7be75-126">Schlanken</span><span class="sxs-lookup"><span data-stu-id="7be75-126">"MP"</span></span>                   | <span data-ttu-id="7be75-127">Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="7be75-127">main profile</span></span>        |
| <span data-ttu-id="7be75-128">2</span><span class="sxs-lookup"><span data-stu-id="7be75-128">2</span></span>                        | <span data-ttu-id="7be75-129">Erfolgen</span><span class="sxs-lookup"><span data-stu-id="7be75-129">"CP"</span></span>                   | <span data-ttu-id="7be75-130">nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="7be75-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7be75-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7be75-131">Requirements</span></span>



| <span data-ttu-id="7be75-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7be75-132">Requirement</span></span> | <span data-ttu-id="7be75-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7be75-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7be75-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7be75-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7be75-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7be75-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7be75-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7be75-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7be75-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7be75-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7be75-138">Header</span><span class="sxs-lookup"><span data-stu-id="7be75-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be75-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be75-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be75-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7be75-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be75-141">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7be75-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




