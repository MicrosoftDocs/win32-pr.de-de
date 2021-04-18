---
description: Unbeschränkte Variablen Bitrate-Codierung
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Unbeschränkte Variablen Bitrate-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343422"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="0f7c7-103">Unbeschränkte Variablen Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="0f7c7-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="0f7c7-104">Im uneingeschränkten VBR-Codierungs Modus wird der Inhalt in die höchste mögliche Qualität codiert, während eine angegebene Bitrate beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="0f7c7-105">Bei der uneingeschränkten VBR-Codierung werden zwei Codierungs Durchgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="0f7c7-106">Wenn Sie die unbeschränkte VBR-Codierung verwenden, geben Sie eine Bitrate für den Stream an, wie bei [konstanter Bitrate-Codierung](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="0f7c7-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="0f7c7-107">Der Encoder verwendet diesen Wert jedoch nur als durchschnittliche Bitrate für den Stream und codiert, sodass die Qualität so hoch wie möglich ist, während der Durchschnitt beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="0f7c7-108">Die einzelnen vom Encoder erstellten Beispiele variieren in der Größe ohne explizite Puffer Limits.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="0f7c7-109">Die durchschnittliche Bitrate während der Codierungs Sitzung und die Dauer des Streams dürfen jedoch nicht größer sein als der von Ihnen angegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="0f7c7-110">Die tatsächliche Bitrate an einem beliebigen Punkt im codierten Stream kann stark vom Durchschnittswert abweichen.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="0f7c7-111">Sie legen kein Puffer Fenster für die nicht eingeschränkte VBR-Codierung fest.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="0f7c7-112">Stattdessen berechnet der Encoder die Größe des erforderlichen Puffer Fensters basierend auf den Anforderungen der codierten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="0f7c7-113">Dies bedeutet, dass es keine Beschränkung auf die Größe der einzelnen Stichproben im Stream gibt, solange die durchschnittliche Bitrate kleiner oder gleich dem Wert ist, den Sie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="0f7c7-114">Der Vorteil der uneingeschränkten VBR-Codierung besteht darin, dass der komprimierte Datenstrom die höchste mögliche Qualität aufweist und gleichzeitig in einer vorhersagbaren durchschnittlichen Bandbreite bleibt.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="0f7c7-115">Verwenden Sie diese Anwendung, wenn Sie eine Bandbreite angeben müssen, aber Schwankungen in Bezug auf die angegebene Bandbreite zulässig sind. beispielsweise für lokale Dateien oder nur für das herunterladen.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="0f7c7-116">Der Nachteil dieses Codierungs Modus besteht darin, dass der Encoder das Puffer Fenster auf einen beliebigen Wert festlegen kann, der nach der Codierung erforderlich ist, sodass Sie keine Kontrolle über die Puffergröße haben.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="0f7c7-117">In den meisten Fällen sollten Sie, wenn Sie sich keine Gedanken über die Größe des Puffers oder die Konsistenz der Bandbreitennutzung machen, die [Qualitäts basierte variierungsbitrate-Codierung](quality-based-variable-bit-rate--vbr--encoding.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="0f7c7-118">Konfigurieren des Encoders für nicht eingeschränkten VBR</span><span class="sxs-lookup"><span data-stu-id="0f7c7-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="0f7c7-119">Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="0f7c7-120">Diese Eigenschaften werden in wmcodecdsp. h definiert.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="0f7c7-121">Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="0f7c7-122">Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0f7c7-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="0f7c7-123">Basierend auf den angegebenen Eigenschafts Werten können Sie die unterstützten VBR-Ausgabetypen auflisten und die erforderliche auf der Grundlage der durchschnittlichen Bitrate auf der Grundlage des Encoders [Media Foundation Transform](media-foundation-transforms.md) (MFT) auswählen.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="0f7c7-124">In der folgenden Liste sind die Eigenschaften aufgeführt, die Sie für diesen Codierungstyp festlegen müssen:</span><span class="sxs-lookup"><span data-stu-id="0f7c7-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="0f7c7-125">Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft mfpkey \_ vbrenabled auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="0f7c7-126">Legen Sie die verwendete mfpkey-Kennung \_ auf 2 fest, da der nicht eingeschränkte VBR-Modus zwei Codierungs Durchläufen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="0f7c7-127">Überprüfen Sie beim Auflisten des Ausgabemedien Typs das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für Audiostreams) oder das Attribut " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) " (für Videostreams) der verfügbaren Ausgabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="0f7c7-128">Wählen Sie einen Ausgabe Medientyp aus, bei dem die durchschnittliche Bitrate der gewünschten durchschnittlichen Bitrate liegt, die der Encoder im codierten Inhalt behalten soll.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="0f7c7-129">Weitere Informationen zum Auswählen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0f7c7-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="0f7c7-130">Um den Puffer Fenster Wert durch den Encoder festzulegen, nennen Sie **iwmcodecleakybucket:: getbuffersizebits**, das in wmcodecigesichter. h und wmcodecdspuuid. lib definiert ist, nach der Codierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="0f7c7-131">Zum Hinzufügen der Unterstützung für nicht eingeschränkte VBR-Datenströme müssen Sie diesen Wert im Attribut " [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) " (durchschnittliche Anzahl der unbeschränkten Bucket-Werte) für das Datenstrom-Konfigurationsobjekt festlegen, während Sie das ASF-Profil konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="0f7c7-132">Im folgenden Beispiel wird die setencodingtype-Methode der Beispiel Klasse cencoder geändert, um den nicht eingeschränkten VBR-Modus einzurichten.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="0f7c7-133">Weitere Informationen zu dieser Klasse finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="0f7c7-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="0f7c7-134">Informationen zu den in diesem Beispiel verwendeten Hilfsmakros finden Sie unter Verwenden der Media Foundation-Code Beispiele.</span><span class="sxs-lookup"><span data-stu-id="0f7c7-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="0f7c7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f7c7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7c7-136">ASF-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="0f7c7-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="0f7c7-137">Das Leaky Bucket-Puffer Modell</span><span class="sxs-lookup"><span data-stu-id="0f7c7-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="0f7c7-138">Erstellen einer Topologie für Two-Pass Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="0f7c7-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



