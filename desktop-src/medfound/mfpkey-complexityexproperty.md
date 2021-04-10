---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215528"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="1da52-103">\_Complexityex-Eigenschaft für mfpkey</span><span class="sxs-lookup"><span data-stu-id="1da52-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="1da52-104">Gibt die Komplexität des Codierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="1da52-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1da52-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1da52-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1da52-106">g \_ wszwmvccomplexityex</span><span class="sxs-lookup"><span data-stu-id="1da52-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="1da52-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1da52-107">Data Type</span></span>

<span data-ttu-id="1da52-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1da52-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1da52-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1da52-109">Default Value</span></span>

<span data-ttu-id="1da52-110">Der Standardwert hängt von der Version des Video Encoders ab, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1da52-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="1da52-111">Codierungs Version</span><span class="sxs-lookup"><span data-stu-id="1da52-111">Encoder version</span></span>                 | <span data-ttu-id="1da52-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1da52-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="1da52-113">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="1da52-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="1da52-114">3</span><span class="sxs-lookup"><span data-stu-id="1da52-114">3</span></span>             |
| <span data-ttu-id="1da52-115">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="1da52-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="1da52-116">1</span><span class="sxs-lookup"><span data-stu-id="1da52-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="1da52-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1da52-117">Possible Values</span></span>

<span data-ttu-id="1da52-118">Die möglichen Werte hängen von der Version des Video Encoders ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1da52-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="1da52-119">Codierungs Version</span><span class="sxs-lookup"><span data-stu-id="1da52-119">Encoder version</span></span>                 | <span data-ttu-id="1da52-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1da52-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="1da52-121">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="1da52-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="1da52-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="1da52-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="1da52-123">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="1da52-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="1da52-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="1da52-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="1da52-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1da52-125">Remarks</span></span>

<span data-ttu-id="1da52-126">Niedrigere Werte bewirken, dass der Codec weniger komplizierte Codierungs Algorithmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1da52-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="1da52-127">Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität verursachen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.</span><span class="sxs-lookup"><span data-stu-id="1da52-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="1da52-128">Dies kann beim Codieren von Inhalten aus einer Live Quelle von Bedeutung sein, da der Encoder Eingaben schnell genug verarbeiten muss, um mit der Quelle zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="1da52-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="1da52-129">Jeder Wert, der dieser Eigenschaft zugewiesen ist, wird ignoriert, wenn die Eigenschaft [ \_ compressionoptimizationtype von mfpkey](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1da52-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="1da52-130">In diesem Fall wird mfpkey \_ complexityex automatisch auf 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1da52-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da52-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1da52-131">Requirements</span></span>



| <span data-ttu-id="1da52-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1da52-132">Requirement</span></span> | <span data-ttu-id="1da52-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1da52-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da52-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1da52-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1da52-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1da52-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1da52-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1da52-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1da52-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1da52-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1da52-138">Header</span><span class="sxs-lookup"><span data-stu-id="1da52-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1da52-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da52-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da52-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1da52-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da52-141">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1da52-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




