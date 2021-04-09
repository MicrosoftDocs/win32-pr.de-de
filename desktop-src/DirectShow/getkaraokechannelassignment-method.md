---
description: Die getkaraokechannelzuweisungs-Methode ruft einen Wert ab, der angibt, wie die Karaoke-Kanäle den Referenten zugewiesen werden.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Getkaraokechannelzuweisungs-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860546"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="3fbaa-103">Getkaraokechannelzuweisungs-Methode</span><span class="sxs-lookup"><span data-stu-id="3fbaa-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="3fbaa-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3fbaa-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3fbaa-106">Die- `GetKaraokeChannelAssignment` Methode ruft einen Wert ab, der angibt, wie die Karaoke-Kanäle den Referenten zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="3fbaa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fbaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbaa-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*</span><span class="sxs-lookup"><span data-stu-id="3fbaa-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="3fbaa-109">Gibt den Audiodatenstrom als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbaa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fbaa-110">Return Value</span></span>

<span data-ttu-id="3fbaa-111">Gibt eine ganze Zahl zurück, die die Lautsprecher Zuweisung für den angegebenen Stream angibt.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="3fbaa-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3fbaa-112">Return code</span></span> | <span data-ttu-id="3fbaa-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fbaa-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3fbaa-114">2</span><span class="sxs-lookup"><span data-stu-id="3fbaa-114">2</span></span>           | <span data-ttu-id="3fbaa-115">Der Stream wird dem linken und rechten Referenten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="3fbaa-116">3</span><span class="sxs-lookup"><span data-stu-id="3fbaa-116">3</span></span>           | <span data-ttu-id="3fbaa-117">Der Stream wird dem linken, rechten und mittleren Referenten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="3fbaa-118">4</span><span class="sxs-lookup"><span data-stu-id="3fbaa-118">4</span></span>           | <span data-ttu-id="3fbaa-119">Der Stream wird dem linken, rechten und audio1-Sprecher zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="3fbaa-120">5</span><span class="sxs-lookup"><span data-stu-id="3fbaa-120">5</span></span>           | <span data-ttu-id="3fbaa-121">Der Stream wird dem linken, rechten, mittleren und audio1-Sprecher zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="3fbaa-122">6</span><span class="sxs-lookup"><span data-stu-id="3fbaa-122">6</span></span>           | <span data-ttu-id="3fbaa-123">Der Stream wird dem linken, rechten und Audio2-Sprecher zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="3fbaa-124">7</span><span class="sxs-lookup"><span data-stu-id="3fbaa-124">7</span></span>           | <span data-ttu-id="3fbaa-125">Der Stream wird dem linken, rechten, mittleren und Audio2-Sprecher zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fbaa-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3fbaa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fbaa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbaa-127">**Karaokeaudiopressentiments ationmode**</span><span class="sxs-lookup"><span data-stu-id="3fbaa-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



