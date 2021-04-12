---
description: Gibt das aktuelle Eingabeformat für den Decoder an.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Avdeccommoninputformat-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482283"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="bb035-103">Avdeccommoninputformat (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb035-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="bb035-104">Gibt das aktuelle Eingabeformat für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="bb035-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="bb035-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bb035-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb035-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bb035-106">Data type</span></span>

<span data-ttu-id="bb035-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="bb035-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bb035-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="bb035-108">Property GUID</span></span>

<span data-ttu-id="bb035-109">**Codecapi \_ avdeccommoninputformat**</span><span class="sxs-lookup"><span data-stu-id="bb035-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="bb035-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bb035-110">Property value</span></span>

<span data-ttu-id="bb035-111">Der Wert dieser Eigenschaft ist ein **BSTR** -Wert, der die Zeichen folgen Darstellung einer GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="bb035-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="bb035-112">Die folgenden GUIDs sind definiert.</span><span class="sxs-lookup"><span data-stu-id="bb035-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="bb035-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="bb035-113">**GUID**</span></span>                                            | <span data-ttu-id="bb035-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb035-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="bb035-115">**Codecapi- \_ GUID \_ avdecaudioinputaac**</span><span class="sxs-lookup"><span data-stu-id="bb035-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="bb035-116">"Advanced audiocoding" (AAC)</span><span class="sxs-lookup"><span data-stu-id="bb035-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="bb035-117">**Codecapi- \_ GUID \_ avdecaudioinputdolbydigitalplus**</span><span class="sxs-lookup"><span data-stu-id="bb035-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="bb035-118">Dolby Digital Plus-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="bb035-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="bb035-119">**Codecapi- \_ GUID \_ avdecaudioinputdolby**</span><span class="sxs-lookup"><span data-stu-id="bb035-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="bb035-120">Dolby-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="bb035-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="bb035-121">**Codecapi- \_ GUID \_ avdecaudioinputdts**</span><span class="sxs-lookup"><span data-stu-id="bb035-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="bb035-122">DTS-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="bb035-122">DTS audio</span></span>                                      |
| <span data-ttu-id="bb035-123">**Codecapi \_ GUID \_ avdecaudioinpuderaac**</span><span class="sxs-lookup"><span data-stu-id="bb035-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="bb035-124">High-Efficiency erweiterte Audiocodierung (HE-AAC)</span><span class="sxs-lookup"><span data-stu-id="bb035-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="bb035-125">**Codecapi- \_ GUID \_ avdecaudioinputmpeg**</span><span class="sxs-lookup"><span data-stu-id="bb035-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="bb035-126">MPEG-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="bb035-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="bb035-127">**Codecapi- \_ GUID \_ avdecaudioinputpcm**</span><span class="sxs-lookup"><span data-stu-id="bb035-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="bb035-128">PCM-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="bb035-128">PCM audio</span></span>                                      |
| <span data-ttu-id="bb035-129">**Codecapi- \_ GUID \_ avdecaudioinputwma**</span><span class="sxs-lookup"><span data-stu-id="bb035-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="bb035-130">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="bb035-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="bb035-131">**Codecapi- \_ GUID \_ avdecaudioinputwmapro**</span><span class="sxs-lookup"><span data-stu-id="bb035-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="bb035-132">Windows Media Audio 9 Professional (WMA Pro)</span><span class="sxs-lookup"><span data-stu-id="bb035-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="bb035-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb035-133">Requirements</span></span>



| <span data-ttu-id="bb035-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb035-134">Requirement</span></span> | <span data-ttu-id="bb035-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bb035-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb035-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb035-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bb035-137">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb035-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bb035-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb035-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bb035-139">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb035-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bb035-140">Header</span><span class="sxs-lookup"><span data-stu-id="bb035-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb035-141"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb035-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb035-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb035-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb035-143">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="bb035-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bb035-144">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bb035-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




