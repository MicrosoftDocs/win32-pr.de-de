---
title: Equalizersettings. Crossfade
description: Mit dem Crossfade-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Kreuz ausblenden aktiviert ist.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- Equalizersettings. Crossfade-Windows-Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367121"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="0731f-104">Equalizersettings. Crossfade</span><span class="sxs-lookup"><span data-stu-id="0731f-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="0731f-105">Mit dem **Crossfade** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Kreuz ausblenden aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0731f-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="0731f-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0731f-106">Possible Values</span></span>

<span data-ttu-id="0731f-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0731f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0731f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0731f-108">Value</span></span> | <span data-ttu-id="0731f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0731f-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="0731f-110">true</span><span class="sxs-lookup"><span data-stu-id="0731f-110">true</span></span>  | <span data-ttu-id="0731f-111">Cross-Fade ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0731f-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="0731f-112">false</span><span class="sxs-lookup"><span data-stu-id="0731f-112">false</span></span> | <span data-ttu-id="0731f-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="0731f-113">Default.</span></span> <span data-ttu-id="0731f-114">Cross-Fade ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0731f-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0731f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0731f-115">Remarks</span></span>

<span data-ttu-id="0731f-116">Cross-Fade ist eine Funktion zur Audioverarbeitung, bei der das Volumen eines Medien Elements nach dem Ende der Wiedergabe allmählich verringert wird, während gleichzeitig die Wiedergabe des nächsten Medien Elements auf dem minimalen Volume gestartet wird und die Daten allmählich auf das normale Volume erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="0731f-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="0731f-117">Die Überlappung zwischen dem Start des zweiten Medien Elements und dem Ende des ersten Medien Elements wird durch das **crossfadewindow** -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="0731f-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="0731f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0731f-118">Requirements</span></span>



| <span data-ttu-id="0731f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0731f-119">Requirement</span></span> | <span data-ttu-id="0731f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0731f-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0731f-121">Version</span><span class="sxs-lookup"><span data-stu-id="0731f-121">Version</span></span><br/> | <span data-ttu-id="0731f-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0731f-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0731f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0731f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0731f-124">**Equalizersettings-Element**</span><span class="sxs-lookup"><span data-stu-id="0731f-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="0731f-125">**Equalizersettings. crossfadewindow**</span><span class="sxs-lookup"><span data-stu-id="0731f-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





