---
description: 'In der Spitzen eingeschränkten Variablen Bitrate (VBR) wird der Inhalt in eine angegebene Bitrate und Spitzenwerte codiert: eine Spitzen Bitrate und ein Spitzen Puffer Fenster.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained Variablen-Bitrate-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347858"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="fe0fa-103">Peak-Constrained Variablen-Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="fe0fa-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="fe0fa-104">In der Spitzen eingeschränkten Variablen Bitrate (VBR) wird der Inhalt in eine angegebene Bitrate und *Spitzenwerte* codiert: eine Spitzen Bitrate und ein Spitzen Puffer Fenster.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="fe0fa-105">Diese Spitzenwerte werden auch als *Maximale Lecky-Bucket-Werte* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="fe0fa-106">Die Datei wird so codiert, dass Sie einem Puffer entspricht, der durch die Spitzenwerte beschrieben wird, sodass die durchschnittliche Bitrate des Streams kleiner oder kleiner als der Wert für die durchschnittliche Bitrate ist, den Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="fe0fa-107">In der Regel ist die Spitzen Bitrate sehr hoch.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="fe0fa-108">Der Encoder stellt sicher, dass der angegebene Wert für die durchschnittliche Bitrate für die Dauer des Streams beibehalten wird (durchschnittliche Bitrate >= (gesamte Streamgröße in Bits/Stream-Dauer in Sekunden)).</span><span class="sxs-lookup"><span data-stu-id="fe0fa-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="fe0fa-109">Sehen Sie sich das folgende Beispiel an: Sie konfigurieren einen Stream mit einer durchschnittlichen Bitrate von 16.000 Bits pro Sekunde, einer Spitzen Bitrate von 48.000 Bits pro Sekunde und einem Spitzen Puffer Fenster von 3.000 (3 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="fe0fa-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="fe0fa-110">Die Größe des für den Stream verwendeten Puffers beträgt 144.000 Bits (48.000 Bits pro Sekunde \* 3 Sekunden), wie durch die Spitzenwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="fe0fa-111">Der Encoder komprimiert die Daten, damit Sie diesem Puffer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="fe0fa-112">Außerdem muss die durchschnittliche Bitrate des Streams 16.000 oder weniger betragen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="fe0fa-113">Wenn der Encoder große Beispiele zum Verarbeiten eines komplexen Inhalts Segments erstellen muss, kann er die große Puffergröße nutzen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="fe0fa-114">Andere Teile des Streams müssen jedoch mit einer niedrigeren Bitrate codiert werden, um den Durchschnitt auf die angegebene Ebene zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="fe0fa-115">Die mit Spitzen Beschränkung beschränkte VBR-Codierung eignet sich für die Wiedergabe von Geräten mit einer begrenzten Pufferkapazität und Datenraten Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="fe0fa-116">Ein gängiges Beispiel hierfür ist die Codierung, die für DVDs verwendet wird, wenn die Decodierung von einem Chip in einem Gerät durchgeführt wird, bei dem Hardware Einschränkungen beachtet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="fe0fa-117">Konfigurieren des Encoders für Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="fe0fa-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="fe0fa-118">VBR mit hoher Einschränkung ist so ähnlich wie der eingeschränkte [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) , da es sich auf eine durchschnittliche Bitrate während der Dauer des Streams beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="fe0fa-119">Darüber hinaus entspricht VBR mit hoher Einschränkung einem Spitzen Puffer.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="fe0fa-120">Dieser Puffer wird mit einer Spitzen Bitrate und einem Spitzen Puffer Fenster beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="fe0fa-121">Dieser Modus verwendet zwei Codierungs Durchläufen und bietet dem Encoder Flexibilität bei der Codierung einzelner Stichproben, während die Spitzen Grenzen einhalten.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="fe0fa-122">Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="fe0fa-123">Diese Eigenschaften werden in wmcodecdsp. h definiert.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="fe0fa-124">Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="fe0fa-125">Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="fe0fa-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="fe0fa-126">Basierend auf den angegebenen Eigenschafts Werten können Sie die unterstützten VBR-Ausgabetypen auflisten und die erforderliche auf der Grundlage der durchschnittlichen Bitrate auf der Grundlage des Encoders [Media Foundation Transform](media-foundation-transforms.md) (MFT) auswählen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="fe0fa-127">Sie müssen die folgenden Eigenschaften für diese Art von Codierung festlegen:</span><span class="sxs-lookup"><span data-stu-id="fe0fa-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="fe0fa-128">Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft mfpkey \_ vbrenabled auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="fe0fa-129">Legen Sie den Wert für "mfpkey" auf "2" fest \_ , da der Modus mit hoher eingeschränkter Verwendung zwei Codierungs Durchläufen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="fe0fa-130">Legen Sie mfpkey \_ Rmax fest, um die maximale Bitrate anzugeben, und legen Sie mfpkey \_ bmax fest, um das Spitzen Puffer Fenster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="fe0fa-131">Überprüfen Sie beim Auflisten des Ausgabemedien Typs das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für audiodatenstreams) oder das " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) "-Attribut (für Videostreams) der verfügbaren Ausgabemedien Typen, und wählen Sie einen Ausgabe Medientyp aus, der der durchschnittlichen Bitrate am nächsten liegt, die der Encoder im codierten Inhalt behalten soll</span><span class="sxs-lookup"><span data-stu-id="fe0fa-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="fe0fa-132">Weitere Informationen zum Auswählen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="fe0fa-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="fe0fa-133">Es wird empfohlen, die Spitzen Bitrate auf mindestens doppelte die durchschnittliche Bitrate festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="fe0fa-134">Wenn die Spitzen Rate auf einen niedrigeren Wert festgelegt wird, codiert der Encoder den Inhalt möglicherweise als zwei-Pass-CBR anstelle von VBR mit eingeschränkter Spitzen Zahl.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="fe0fa-135">Um den vom Encoder festgelegten Puffer Fenster Wert abzurufen, nennen Sie nach der Codierungs Sitzung **iwmcodecleakybucket:: getbuffersizebits**, das in wmcodecigesichter. h, wmcodecdspuuid. lib, definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="fe0fa-136">Zum Hinzufügen der Unterstützung für nicht eingeschränkte VBR-Datenströme müssen Sie diesen Wert im " [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) "-Attribut (maximale Anzahl von unbeschränkten Bucket-Werten) für das Datenstrom-Konfigurationsobjekt festlegen, während Sie das ASF-Profil konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="fe0fa-137">Im folgenden Codebeispiel wird die setencodingtype-Methode der Beispiel Klasse cencoder geändert, um den VBR-Modus mit hoher Auslastung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="fe0fa-138">Weitere Informationen zu dieser Klasse finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="fe0fa-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="fe0fa-139">Informationen zu den in diesem Beispiel verwendeten Hilfsmakros finden Sie unter Verwenden der Media Foundation-Code Beispiele.</span><span class="sxs-lookup"><span data-stu-id="fe0fa-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
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

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="fe0fa-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe0fa-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe0fa-141">ASF-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="fe0fa-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="fe0fa-142">Das Leaky Bucket-Puffer Modell</span><span class="sxs-lookup"><span data-stu-id="fe0fa-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="fe0fa-143">Erstellen einer Topologie für Two-Pass Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="fe0fa-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



