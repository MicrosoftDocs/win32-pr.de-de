---
description: Gibt das Ausgabeformat für den Decoder an.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Avdeccommonoutputformat-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522480"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="c6613-103">Avdeccommonoutputformat (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6613-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="c6613-104">Gibt das Ausgabeformat für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="c6613-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="c6613-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c6613-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6613-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c6613-106">Data type</span></span>

<span data-ttu-id="c6613-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c6613-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c6613-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="c6613-108">Property GUID</span></span>

<span data-ttu-id="c6613-109">**Codecapi \_ avdeccommonoutputformat**</span><span class="sxs-lookup"><span data-stu-id="c6613-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="c6613-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c6613-110">Property value</span></span>



| <span data-ttu-id="c6613-111">GUID</span><span class="sxs-lookup"><span data-stu-id="c6613-111">GUID</span></span>                                                               | <span data-ttu-id="c6613-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6613-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6613-113">Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM</span><span class="sxs-lookup"><span data-stu-id="c6613-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="c6613-114">PCM-Audiodaten mit beliebig vielen Kanälen</span><span class="sxs-lookup"><span data-stu-id="c6613-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="c6613-115">Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM- \_ Kopfhörer</span><span class="sxs-lookup"><span data-stu-id="c6613-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="c6613-116">Stereo-PCM-Audiodaten, verwenden von left-only/Right (LO/RO)-Downmix</span><span class="sxs-lookup"><span data-stu-id="c6613-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="c6613-117">Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM \_ Stereo \_ Auto</span><span class="sxs-lookup"><span data-stu-id="c6613-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="c6613-118">Stereo PCM-Audiodatei mit automatischer Auswahl des Stereo-downmischmodus (LO/RO oder lt/RT).</span><span class="sxs-lookup"><span data-stu-id="c6613-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="c6613-119">Sie können diesen Wert für Audioformate verwenden, in denen der Eingabestream den bevorzugten downmischungs Modus definiert, z. b. Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="c6613-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="c6613-120">Codecapi \_ GUID \_ avdecaudiooutputformat \_ PCM \_ Stereo \_ matrixencoded</span><span class="sxs-lookup"><span data-stu-id="c6613-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="c6613-121">Stereo PCM-Audiodatei mit Matrix codiertem Stereo Downmix (LT/RT)</span><span class="sxs-lookup"><span data-stu-id="c6613-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="c6613-122">Codecapi \_ GUID \_ avdecaudiooutputformat \_ SPDIF \_ Bitstream</span><span class="sxs-lookup"><span data-stu-id="c6613-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="c6613-123">S/PDIF (Sony/Philips Digital Interface Format) komprimierter Bitstream, wie von IEC-60958 definiert</span><span class="sxs-lookup"><span data-stu-id="c6613-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="c6613-124">Codecapi \_ GUID \_ avdecaudiooutputformat \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="c6613-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="c6613-125">E/a PDIF PCM Stereo, gemäß IEC-60958</span><span class="sxs-lookup"><span data-stu-id="c6613-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="c6613-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6613-126">Requirements</span></span>



| <span data-ttu-id="c6613-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6613-127">Requirement</span></span> | <span data-ttu-id="c6613-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c6613-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6613-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6613-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6613-130">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6613-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c6613-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6613-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6613-132">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c6613-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c6613-133">Header</span><span class="sxs-lookup"><span data-stu-id="c6613-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6613-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6613-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6613-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6613-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6613-136">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="c6613-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c6613-137">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c6613-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




