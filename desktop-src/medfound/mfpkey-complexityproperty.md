---
description: 'MFPKEY_COMPLEXITY-Eigenschaft: Gibt die Komplexität des Encoderalgorithmus an.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092938"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="9cfc0-103">MFPKEY \_ COMPLEXITY-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cfc0-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="9cfc0-104">\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9cfc0-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9cfc0-106">Verwenden Sie stattdessen **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="9cfc0-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="9cfc0-107">Gibt die Komplexität des Encoderalgorithmus an.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9cfc0-108">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9cfc0-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="9cfc0-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="9cfc0-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="9cfc0-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9cfc0-110">Data Type</span></span>

<span data-ttu-id="9cfc0-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9cfc0-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9cfc0-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9cfc0-112">Default Value</span></span>

<span data-ttu-id="9cfc0-113">Der Standardwert hängt von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="9cfc0-114">Encoderversion</span><span class="sxs-lookup"><span data-stu-id="9cfc0-114">Encoder version</span></span>                 | <span data-ttu-id="9cfc0-115">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9cfc0-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="9cfc0-116">Windows Media Video 9-Encoder</span><span class="sxs-lookup"><span data-stu-id="9cfc0-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="9cfc0-117">3</span><span class="sxs-lookup"><span data-stu-id="9cfc0-117">3</span></span>             |
| <span data-ttu-id="9cfc0-118">Windows Media Video 7/8-Encoder</span><span class="sxs-lookup"><span data-stu-id="9cfc0-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="9cfc0-119">1</span><span class="sxs-lookup"><span data-stu-id="9cfc0-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="9cfc0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cfc0-120">Remarks</span></span>

<span data-ttu-id="9cfc0-121">Dieser ganzzahlige Wert liegt zwischen 0 und 3.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="9cfc0-122">Niedrigere Werte führen dazu, dass der Codec weniger komplizierte Codierungsalgorithmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="9cfc0-123">Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität erzeugen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.</span><span class="sxs-lookup"><span data-stu-id="9cfc0-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cfc0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cfc0-124">Requirements</span></span>



| <span data-ttu-id="9cfc0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cfc0-125">Requirement</span></span> | <span data-ttu-id="9cfc0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9cfc0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfc0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cfc0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9cfc0-128">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cfc0-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9cfc0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cfc0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9cfc0-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cfc0-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9cfc0-131">Header</span><span class="sxs-lookup"><span data-stu-id="9cfc0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cfc0-132"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9cfc0-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cfc0-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9cfc0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cfc0-134">Media Foundation Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cfc0-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




