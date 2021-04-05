---
description: Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755496"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="8476b-103">Mfpkey \_ Color-v- \_ Modus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8476b-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="8476b-104">Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8476b-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8476b-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8476b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8476b-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8476b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8476b-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8476b-107">Data Type</span></span>

<span data-ttu-id="8476b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8476b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8476b-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="8476b-109">Default Value</span></span>

<span data-ttu-id="8476b-110">Wird vom DSP aus dem Quellvideo berechnet.</span><span class="sxs-lookup"><span data-stu-id="8476b-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8476b-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="8476b-111">Applies To</span></span>

-   [<span data-ttu-id="8476b-112">Farb Konverter-DSP</span><span class="sxs-lookup"><span data-stu-id="8476b-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="8476b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8476b-113">Remarks</span></span>

<span data-ttu-id="8476b-114">Verwenden Sie einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="8476b-114">Use one of the following values.</span></span>



| <span data-ttu-id="8476b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8476b-115">Value</span></span> | <span data-ttu-id="8476b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8476b-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="8476b-117">0</span><span class="sxs-lookup"><span data-stu-id="8476b-117">0</span></span>     | <span data-ttu-id="8476b-118">progressiv</span><span class="sxs-lookup"><span data-stu-id="8476b-118">Progressive</span></span> |
| <span data-ttu-id="8476b-119">2</span><span class="sxs-lookup"><span data-stu-id="8476b-119">2</span></span>     | <span data-ttu-id="8476b-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="8476b-120">Interlaced</span></span>  |



 

<span data-ttu-id="8476b-121">Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabe Medientyp, um zu bestimmen, ob das Video mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8476b-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="8476b-122">Sie können diese Eigenschaft festlegen, um die Medientyp Einstellung außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="8476b-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="8476b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8476b-123">Requirements</span></span>



| <span data-ttu-id="8476b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8476b-124">Requirement</span></span> | <span data-ttu-id="8476b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8476b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8476b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8476b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8476b-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8476b-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8476b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8476b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8476b-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8476b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8476b-130">Header</span><span class="sxs-lookup"><span data-stu-id="8476b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8476b-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8476b-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8476b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8476b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8476b-133">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8476b-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
