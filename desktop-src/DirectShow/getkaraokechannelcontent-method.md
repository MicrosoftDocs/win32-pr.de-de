---
description: Die getkaraokechannelcontent-Methode ruft einen Wert ab, der den Inhaltstyp im angegebenen Datenstrom im angegebenen Karaoke-Channel angibt.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Getkaraokechannelcontent-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346599"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="fce80-103">Getkaraokechannelcontent-Methode</span><span class="sxs-lookup"><span data-stu-id="fce80-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="fce80-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fce80-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fce80-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fce80-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fce80-106">Die- `GetKaraokeChannelContent` Methode ruft einen Wert ab, der den Inhaltstyp im angegebenen Datenstrom im angegebenen Karaoke-Channel angibt.</span><span class="sxs-lookup"><span data-stu-id="fce80-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="fce80-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce80-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce80-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*</span><span class="sxs-lookup"><span data-stu-id="fce80-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="fce80-109">Gibt den Audiodatenstrom als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="fce80-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="fce80-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*IChannel*</span><span class="sxs-lookup"><span data-stu-id="fce80-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="fce80-111">Gibt den Kanal als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="fce80-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="fce80-112">Die möglichen Werte für jeden Kanal lauten:</span><span class="sxs-lookup"><span data-stu-id="fce80-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="fce80-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fce80-113">Value</span></span>  | <span data-ttu-id="fce80-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fce80-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="fce80-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="fce80-115">0x0001</span></span> | <span data-ttu-id="fce80-116">Leitfaden 1</span><span class="sxs-lookup"><span data-stu-id="fce80-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="fce80-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="fce80-117">0x0002</span></span> | <span data-ttu-id="fce80-118">Leitfaden für Gesang 2</span><span class="sxs-lookup"><span data-stu-id="fce80-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="fce80-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="fce80-119">0x0004</span></span> | <span data-ttu-id="fce80-120">Hand Buch-Melodie 1</span><span class="sxs-lookup"><span data-stu-id="fce80-120">Guide Melody 1</span></span> |
| <span data-ttu-id="fce80-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="fce80-121">0x0008</span></span> | <span data-ttu-id="fce80-122">Führungslinie 2</span><span class="sxs-lookup"><span data-stu-id="fce80-122">Guide Melody 2</span></span> |
| <span data-ttu-id="fce80-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="fce80-123">0x0010</span></span> | <span data-ttu-id="fce80-124">Leitfaden für die Anleitung A</span><span class="sxs-lookup"><span data-stu-id="fce80-124">Guide Melody A</span></span> |
| <span data-ttu-id="fce80-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="fce80-125">0x0020</span></span> | <span data-ttu-id="fce80-126">Führungslinie B</span><span class="sxs-lookup"><span data-stu-id="fce80-126">Guide Melody B</span></span> |
| <span data-ttu-id="fce80-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="fce80-127">0x0040</span></span> | <span data-ttu-id="fce80-128">Sound Effekt A</span><span class="sxs-lookup"><span data-stu-id="fce80-128">Sound Effect A</span></span> |
| <span data-ttu-id="fce80-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="fce80-129">0x0080</span></span> | <span data-ttu-id="fce80-130">Sound Effekt B</span><span class="sxs-lookup"><span data-stu-id="fce80-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce80-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fce80-131">Return Value</span></span>

<span data-ttu-id="fce80-132">Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits den Inhalt des Karaoke-Kanals angeben.</span><span class="sxs-lookup"><span data-stu-id="fce80-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce80-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fce80-133">Remarks</span></span>

<span data-ttu-id="fce80-134">Die Nummerierung des DVD-Audiokanals ist NULL basiert, sodass die Kanäle 2, 3 und 4 die zusätzlichen Karaoke-Kanäle sind.</span><span class="sxs-lookup"><span data-stu-id="fce80-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="fce80-135">Führen Sie nach dem Zurückgeben der Methode eine bitweise AND-Operation für *icontent* aus, um den Inhalt der einzelnen Kanäle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fce80-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="fce80-136">Da in einem einzelnen Kanal möglicherweise mehr als ein Inhaltstyp aufgezeichnet wurde, sollten Sie alle möglichen Werte testen, auch nachdem eine Entsprechung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="fce80-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="fce80-137">Nachdem der Benutzer die Inhalte der einzelnen Kanäle kennt, muss er das Volume anpassen oder die einzelnen Kanäle bei Bedarf ein-oder ausschalten können.</span><span class="sxs-lookup"><span data-stu-id="fce80-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="fce80-138">Implementieren Sie diese Funktionalität in Ihrer Anwendung, indem Sie die Eigenschaft " [**karaokeaudiopresentationmode**](karaokeaudiopresentationmode-property.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="fce80-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="fce80-139">Zum Wiedergeben von Karaoke-Festplatten muss der Audiodecoder im System des Benutzers mit der "DirectShow 8"-Karaoke-Implementierung kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="fce80-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



