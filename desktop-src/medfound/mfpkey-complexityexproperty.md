---
description: 'MFPKEY_COMPLEXITYEX-Eigenschaft: Gibt die Komplexität des Encoderalgorithmus an.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087608"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="cd6a3-103">MFPKEY \_ COMPLEXITYEX-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd6a3-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="cd6a3-104">Gibt die Komplexität des Encoderalgorithmus an.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cd6a3-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cd6a3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cd6a3-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="cd6a3-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="cd6a3-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cd6a3-107">Data Type</span></span>

<span data-ttu-id="cd6a3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cd6a3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="cd6a3-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="cd6a3-109">Default Value</span></span>

<span data-ttu-id="cd6a3-110">Der Standardwert hängt von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="cd6a3-111">Encoderversion</span><span class="sxs-lookup"><span data-stu-id="cd6a3-111">Encoder version</span></span>                 | <span data-ttu-id="cd6a3-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="cd6a3-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="cd6a3-113">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="cd6a3-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="cd6a3-114">3</span><span class="sxs-lookup"><span data-stu-id="cd6a3-114">3</span></span>             |
| <span data-ttu-id="cd6a3-115">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="cd6a3-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="cd6a3-116">1</span><span class="sxs-lookup"><span data-stu-id="cd6a3-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="cd6a3-117">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="cd6a3-117">Possible Values</span></span>

<span data-ttu-id="cd6a3-118">Die möglichen Werte hängen von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="cd6a3-119">Encoderversion</span><span class="sxs-lookup"><span data-stu-id="cd6a3-119">Encoder version</span></span>                 | <span data-ttu-id="cd6a3-120">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="cd6a3-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="cd6a3-121">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="cd6a3-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="cd6a3-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="cd6a3-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="cd6a3-123">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="cd6a3-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="cd6a3-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="cd6a3-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="cd6a3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd6a3-125">Remarks</span></span>

<span data-ttu-id="cd6a3-126">Niedrigere Werte führen dazu, dass der Codec weniger komplizierte Codierungsalgorithmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="cd6a3-127">Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität erzeugen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="cd6a3-128">Dies kann wichtig sein, wenn Inhalte aus einer Livequelle codiert werden, da der Encoder Eingaben schnell genug verarbeiten muss, um mit der Quelle Schritt zu halten.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="cd6a3-129">Jeder dieser Eigenschaft zugewiesene Wert wird ignoriert, wenn die [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="cd6a3-130">In diesem Fall wird MFPKEY \_ COMPLEXITYEX automatisch auf 3 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cd6a3-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6a3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd6a3-131">Requirements</span></span>



| <span data-ttu-id="cd6a3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd6a3-132">Requirement</span></span> | <span data-ttu-id="cd6a3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cd6a3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6a3-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd6a3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6a3-135">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cd6a3-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd6a3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6a3-137">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd6a3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd6a3-138">Header</span><span class="sxs-lookup"><span data-stu-id="cd6a3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd6a3-139"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="cd6a3-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6a3-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd6a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6a3-141">Media Foundation-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd6a3-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




