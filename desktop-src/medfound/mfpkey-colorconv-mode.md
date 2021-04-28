---
description: 'MFPKEY_COLORCONV_MODE-Eigenschaft: Gibt an, ob der Eingabestream übersprungen wird.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087578"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="892fb-103">MFPKEY \_ COLORCONV \_ MODE-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="892fb-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="892fb-104">Gibt an, ob der Eingabestream übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="892fb-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="892fb-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="892fb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="892fb-106">Nur mithilfe von [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="892fb-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="892fb-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="892fb-107">Data Type</span></span>

<span data-ttu-id="892fb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="892fb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="892fb-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="892fb-109">Default Value</span></span>

<span data-ttu-id="892fb-110">Wird vom DSP aus dem Quellvideo berechnet.</span><span class="sxs-lookup"><span data-stu-id="892fb-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="892fb-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="892fb-111">Applies To</span></span>

-   [<span data-ttu-id="892fb-112">Farbkonverter-DSP</span><span class="sxs-lookup"><span data-stu-id="892fb-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="892fb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="892fb-113">Remarks</span></span>

<span data-ttu-id="892fb-114">Verwenden Sie einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="892fb-114">Use one of the following values.</span></span>



| <span data-ttu-id="892fb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="892fb-115">Value</span></span> | <span data-ttu-id="892fb-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="892fb-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="892fb-117">0</span><span class="sxs-lookup"><span data-stu-id="892fb-117">0</span></span>     | <span data-ttu-id="892fb-118">progressiv</span><span class="sxs-lookup"><span data-stu-id="892fb-118">Progressive</span></span> |
| <span data-ttu-id="892fb-119">2</span><span class="sxs-lookup"><span data-stu-id="892fb-119">2</span></span>     | <span data-ttu-id="892fb-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="892fb-120">Interlaced</span></span>  |



 

<span data-ttu-id="892fb-121">Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabemedientyp, um zu bestimmen, ob das Video übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="892fb-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="892fb-122">Sie können diese Eigenschaft festlegen, um die Medientypeinstellung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="892fb-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="892fb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="892fb-123">Requirements</span></span>



| <span data-ttu-id="892fb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="892fb-124">Requirement</span></span> | <span data-ttu-id="892fb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="892fb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="892fb-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="892fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="892fb-127">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="892fb-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="892fb-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="892fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="892fb-129">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="892fb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="892fb-130">Header</span><span class="sxs-lookup"><span data-stu-id="892fb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="892fb-131"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="892fb-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="892fb-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="892fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892fb-133">Media Foundation-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="892fb-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
