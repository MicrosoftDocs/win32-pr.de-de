---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215527"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="228d1-103">Mfpkey- \_ Komplexitäts Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="228d1-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="228d1-104">\[[**Mfpkey \_ Die Komplexität**](mfpkey-complexityexproperty.md) ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="228d1-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="228d1-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="228d1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="228d1-106">Verwenden Sie stattdessen **mfpkey \_ complexityex**.\]</span><span class="sxs-lookup"><span data-stu-id="228d1-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="228d1-107">Gibt die Komplexität des Codierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="228d1-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="228d1-108">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="228d1-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="228d1-109">g \_ wszwmvccomplexitymode</span><span class="sxs-lookup"><span data-stu-id="228d1-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="228d1-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="228d1-110">Data Type</span></span>

<span data-ttu-id="228d1-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="228d1-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="228d1-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="228d1-112">Default Value</span></span>

<span data-ttu-id="228d1-113">Der Standardwert hängt von der Version des Video Encoders ab, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="228d1-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="228d1-114">Codierungs Version</span><span class="sxs-lookup"><span data-stu-id="228d1-114">Encoder version</span></span>                 | <span data-ttu-id="228d1-115">Standardwert</span><span class="sxs-lookup"><span data-stu-id="228d1-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="228d1-116">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="228d1-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="228d1-117">3</span><span class="sxs-lookup"><span data-stu-id="228d1-117">3</span></span>             |
| <span data-ttu-id="228d1-118">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="228d1-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="228d1-119">1</span><span class="sxs-lookup"><span data-stu-id="228d1-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="228d1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="228d1-120">Remarks</span></span>

<span data-ttu-id="228d1-121">Dieser ganzzahlige Wert liegt zwischen 0 und 3.</span><span class="sxs-lookup"><span data-stu-id="228d1-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="228d1-122">Niedrigere Werte bewirken, dass der Codec weniger komplizierte Codierungs Algorithmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="228d1-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="228d1-123">Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität verursachen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.</span><span class="sxs-lookup"><span data-stu-id="228d1-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="228d1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="228d1-124">Requirements</span></span>



| <span data-ttu-id="228d1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="228d1-125">Requirement</span></span> | <span data-ttu-id="228d1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="228d1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="228d1-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="228d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="228d1-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="228d1-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="228d1-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="228d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="228d1-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="228d1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="228d1-131">Header</span><span class="sxs-lookup"><span data-stu-id="228d1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="228d1-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="228d1-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228d1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="228d1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228d1-134">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="228d1-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




