---
title: Equalizersettings. Normalisierung
description: Das normalisierungs Attribut gibt einen Wert an, der angibt, ob Normalisierung aktiviert ist, oder ruft diesen ab.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- Equalizersettings. Normalisierung Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359284"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="28b6a-104">Equalizersettings. Normalisierung</span><span class="sxs-lookup"><span data-stu-id="28b6a-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="28b6a-105">Das **normalisierungs** Attribut gibt einen Wert an, der angibt, ob Normalisierung aktiviert ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="28b6a-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="28b6a-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="28b6a-106">Possible Values</span></span>

<span data-ttu-id="28b6a-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="28b6a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="28b6a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="28b6a-108">Value</span></span> | <span data-ttu-id="28b6a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28b6a-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="28b6a-110">true</span><span class="sxs-lookup"><span data-stu-id="28b6a-110">true</span></span>  | <span data-ttu-id="28b6a-111">Normalisierung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="28b6a-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="28b6a-112">false</span><span class="sxs-lookup"><span data-stu-id="28b6a-112">false</span></span> | <span data-ttu-id="28b6a-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="28b6a-113">Default.</span></span> <span data-ttu-id="28b6a-114">Die Normalisierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="28b6a-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="28b6a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28b6a-115">Remarks</span></span>

<span data-ttu-id="28b6a-116">Wenn die Normalisierung aktiviert ist, wird das Audiosignal für eine gesamte digitale Mediendatei auf den maximalen Wert hochskaliert.</span><span class="sxs-lookup"><span data-stu-id="28b6a-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="28b6a-117">Auf diese Weise können mehrere Dateien auf ungefähr demselben Volume abgespielt werden, ohne dass die volumeanpassungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="28b6a-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b6a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28b6a-118">Requirements</span></span>



| <span data-ttu-id="28b6a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28b6a-119">Requirement</span></span> | <span data-ttu-id="28b6a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="28b6a-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="28b6a-121">Version</span><span class="sxs-lookup"><span data-stu-id="28b6a-121">Version</span></span><br/> | <span data-ttu-id="28b6a-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="28b6a-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28b6a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28b6a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b6a-124">**Equalizersettings-Element**</span><span class="sxs-lookup"><span data-stu-id="28b6a-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="28b6a-125">**Equalizersettings. normalizationaverage**</span><span class="sxs-lookup"><span data-stu-id="28b6a-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="28b6a-126">**Equalizersettings. normalizationpeak**</span><span class="sxs-lookup"><span data-stu-id="28b6a-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





