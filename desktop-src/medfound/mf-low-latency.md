---
description: Ermöglicht die Verarbeitung mit niedriger Latenz in der Microsoft Media Foundation Pipeline.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757866"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="7bd2c-103">\_Attribut mit geringer Latenz bei MF \_</span><span class="sxs-lookup"><span data-stu-id="7bd2c-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="7bd2c-104">Ermöglicht die Verarbeitung mit niedriger Latenz in der Microsoft Media Foundation Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="7bd2c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7bd2c-105">Data type</span></span>

<span data-ttu-id="7bd2c-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bd2c-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7bd2c-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="7bd2c-107">Get/set</span></span>

<span data-ttu-id="7bd2c-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7bd2c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7bd2c-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7bd2c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd2c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bd2c-110">Remarks</span></span>

<span data-ttu-id="7bd2c-111">Geringe Latenzzeit wird als kleinste mögliche Verzögerung beim Generieren (oder empfangen) der Mediendaten beim Rendern definiert.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="7bd2c-112">Geringe Latenzzeit ist für echt Zeit Kommunikationsszenarien wünschenswert.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="7bd2c-113">In anderen Szenarien, wie z. b. der lokalen Wiedergabe oder der Transcodierung, sollten Sie in der Regel den Modus mit niedriger Latenz nicht aktivieren, da dies die Qualität beeinflussen kann.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="7bd2c-114">Der GUID-Wert dieses Attributs ist mit der Eigenschaft " [codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md) " identisch, die für die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="7bd2c-115">Legen Sie dieses Attribut für Pipeline Komponenten wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="7bd2c-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="7bd2c-116">Medienquelle: Verwenden Sie die [**imfmediasourceex:: getsourceattributormethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="7bd2c-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="7bd2c-117">Media Foundation Transformation (MFT): Verwenden Sie die [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="7bd2c-118">Bei Encodern unterstützt der Encoder möglicherweise eine geringe Latenzzeit über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="7bd2c-119">Medien Senke: Abfragen der Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="7bd2c-120">Anwendungen legen dieses Attribut in der Regel nicht direkt auf den Pipeline Komponenten fest, sondern legen stattdessen das-Attribut für eines der folgenden Objekte fest:</span><span class="sxs-lookup"><span data-stu-id="7bd2c-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="7bd2c-121">[Medien Sitzung](media-session.md): Verwenden Sie den *pkonfigurations* -Parameter der [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) -oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion, oder legen Sie das-Attribut in der Topologie fest.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="7bd2c-122">[Quell Leser](source-reader.md): Legen Sie das-Attribut mit den Konfigurations Eigenschaften beim Erstellen des Quell Readers fest.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="7bd2c-123">Weitere Informationen finden Sie unter [Attribute des Quell Readers](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7bd2c-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="7bd2c-124">[Sink Writer](sink-writer.md): Legen Sie das-Attribut mit den Konfigurations Eigenschaften fest, wenn Sie den Senke-Writer erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="7bd2c-125">Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7bd2c-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd2c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bd2c-126">Requirements</span></span>



| <span data-ttu-id="7bd2c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bd2c-127">Requirement</span></span> | <span data-ttu-id="7bd2c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7bd2c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd2c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bd2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd2c-130">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd2c-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7bd2c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bd2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd2c-132">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7bd2c-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7bd2c-133">Header</span><span class="sxs-lookup"><span data-stu-id="7bd2c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bd2c-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bd2c-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd2c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd2c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd2c-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7bd2c-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bd2c-137">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="7bd2c-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bd2c-138">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="7bd2c-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bd2c-139">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="7bd2c-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
