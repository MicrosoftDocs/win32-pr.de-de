---
description: Mit der Eigenschaft "karaokeaudiopressentiments ationmode" wird die "right left Speaker"-Mischung für die zusätzlichen Karaoke-Kanäle festgelegt oder abgerufen.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Karaokeaudiopressentiments ationmode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343546"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="d14e1-103">Karaokeaudiopressentiments ationmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d14e1-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="d14e1-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d14e1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d14e1-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d14e1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d14e1-106">Die- `KaraokeAudioPresentationMode` Eigenschaft legt den Rechts linken sprechermix für die zusätzlichen Karaoke-Kanäle fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d14e1-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="d14e1-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d14e1-107">Return Value</span></span>

<span data-ttu-id="d14e1-108">Gibt einen ganzzahligen Wert mit einem Satz von Bitflags zurück, der angibt, wie die zusätzlichen Karaoke-Kanäle auf den linken und rechten Referenten herabgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="d14e1-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="d14e1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d14e1-109">Remarks</span></span>

<span data-ttu-id="d14e1-110">Diese Eigenschaft ist Lese-/Schreibzugriff mit dem Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d14e1-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="d14e1-111">Audiokanäle sind NULL basiert, sodass die Kanäle 0 und 1 im Allgemeinen die Kanäle für den rechten und linken Sprecher darstellen und die Kanäle 2 bis 4 die drei zusätzlichen Karaoke-Kanäle sind.</span><span class="sxs-lookup"><span data-stu-id="d14e1-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="d14e1-112">Wenn das mswebdvd-Objekt in den Modus "Karaoke" wechselt, werden die Kanäle 2 und höher automatisch mit einem Mutes</span><span class="sxs-lookup"><span data-stu-id="d14e1-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="d14e1-113">Verwenden Sie bitweise **or** -Vorgänge, um das entsprechende Bit festzulegen, um einen hilfsanchannel an den linken Sprecher, den rechten Sprecher, beide Sprecher (beide Bits on) oder an keine Sprecher (beide Bits off) zu senden.</span><span class="sxs-lookup"><span data-stu-id="d14e1-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="d14e1-114">Diese Bits sind standardmäßig deaktiviert, wenn der DVD-Navigator in den Karaoke-Modus wechselt.</span><span class="sxs-lookup"><span data-stu-id="d14e1-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="d14e1-115">Der Wert der Bits und die entsprechende Aktion werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="d14e1-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="d14e1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d14e1-116">Value</span></span>  | <span data-ttu-id="d14e1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d14e1-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="d14e1-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="d14e1-118">0x0004</span></span> | <span data-ttu-id="d14e1-119">Downmix von Channel 2 zum linken Sprecher</span><span class="sxs-lookup"><span data-stu-id="d14e1-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="d14e1-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="d14e1-120">0x0008</span></span> | <span data-ttu-id="d14e1-121">Downmix von Channel 3 zum linken Sprecher</span><span class="sxs-lookup"><span data-stu-id="d14e1-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="d14e1-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="d14e1-122">0x0010</span></span> | <span data-ttu-id="d14e1-123">Downmix von Channel 4 zum linken Sprecher</span><span class="sxs-lookup"><span data-stu-id="d14e1-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="d14e1-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="d14e1-124">0x0400</span></span> | <span data-ttu-id="d14e1-125">Downmix von Channel 2 zum rechten Redner</span><span class="sxs-lookup"><span data-stu-id="d14e1-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="d14e1-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="d14e1-126">0x0800</span></span> | <span data-ttu-id="d14e1-127">Downmix von Channel 3 zum rechten Redner</span><span class="sxs-lookup"><span data-stu-id="d14e1-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="d14e1-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="d14e1-128">0x1000</span></span> | <span data-ttu-id="d14e1-129">Downmix von Channel 4 zum rechten Redner</span><span class="sxs-lookup"><span data-stu-id="d14e1-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



