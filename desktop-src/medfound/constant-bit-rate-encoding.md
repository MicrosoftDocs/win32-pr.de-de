---
description: Konstante Bitrate-Codierung
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Konstante Bitrate-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958652"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="1a115-103">Konstante Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="1a115-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="1a115-104">Bei der Codierung mit konstanter Bitrate (CBR) kennt der Encoder die Bitrate der Ausgabemedien Beispiele und das Puffer Fenster ("Leaky Bucket Parameters"), bevor die Codierungs Sitzung beginnt.</span><span class="sxs-lookup"><span data-stu-id="1a115-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="1a115-105">Der Encoder verwendet die gleiche Anzahl von Bits, um jede Sekunde von Sample während der gesamten Dauer der Datei zu codieren, um die Zielbitrate für einen Datenstrom zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1a115-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="1a115-106">Dies schränkt die Variation der Größe der streambeispiele ein.</span><span class="sxs-lookup"><span data-stu-id="1a115-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="1a115-107">Außerdem liegt die Bitrate während der Codierungs Sitzung nicht genau beim angegebenen Wert, sondern bleibt in der Nähe der Zielbitrate.</span><span class="sxs-lookup"><span data-stu-id="1a115-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="1a115-108">CBR-Codierung ist hilfreich, wenn Sie die Bitrate oder die geschätzte Dauer einer Datei herausfinden möchten, ohne die gesamte Datei zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="1a115-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="1a115-109">Dies wird z. B. beim Livestreaming benötigt, wenn die Medieninhalte mit einer vorhersehbaren Bitrate und mit konstanter Bandbreitennutzung gestreamt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1a115-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="1a115-110">Der Nachteil der CBR-Codierung besteht darin, dass die Qualität des codierten Inhalts nicht konstant ist.</span><span class="sxs-lookup"><span data-stu-id="1a115-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="1a115-111">Da es schwieriger ist, Inhalte zu komprimieren, sind Teile eines CBR-Streams von geringerer Qualität als andere.</span><span class="sxs-lookup"><span data-stu-id="1a115-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="1a115-112">Ein typischer Film hat z. b. einige Szenen, die relativ statisch sind, und einige Szenen, die vollständig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1a115-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="1a115-113">Wenn Sie einen Film mit CBR codieren, sind die Szenen, die statisch und somit leicht zu codieren sind, von höherer Qualität als die Aktions Szenen, die für die Beibehaltung der gleichen Qualität eine höhere Stichprobengröße erfordern.</span><span class="sxs-lookup"><span data-stu-id="1a115-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="1a115-114">Im Allgemeinen sind Variationen der Qualität einer CBR-Datei in niedrigeren Bitraten deutlicher ausgeprägt.</span><span class="sxs-lookup"><span data-stu-id="1a115-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="1a115-115">Bei höheren Bitraten variiert die Qualität einer CBR-codierten Datei weiterhin, aber die Qualitätsprobleme sind für den Benutzer weniger bemerkbar.</span><span class="sxs-lookup"><span data-stu-id="1a115-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="1a115-116">Wenn Sie die CBR-Codierung verwenden, sollten Sie die Bandbreite so hoch festlegen, dass Sie das Liefer Szenario zulässt.</span><span class="sxs-lookup"><span data-stu-id="1a115-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="1a115-117">CBR-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="1a115-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="1a115-118">Einstellungen für "Leaky Bucket"</span><span class="sxs-lookup"><span data-stu-id="1a115-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="1a115-119">CBR-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="1a115-119">CBR Configuration Settings</span></span>

<span data-ttu-id="1a115-120">Sie müssen einen Encoder konfigurieren, indem Sie den Codierungstyp und die verschiedenen streamspezifischen Einstellungen vor der Codierungs Sitzung angeben.</span><span class="sxs-lookup"><span data-stu-id="1a115-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="1a115-121">**So konfigurieren Sie den Encoder für die CBR-Codierung**</span><span class="sxs-lookup"><span data-stu-id="1a115-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="1a115-122">Geben Sie den CBR-Codierungs Modus an.</span><span class="sxs-lookup"><span data-stu-id="1a115-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="1a115-123">Standardmäßig ist der Encoder für die Verwendung der CBR-Codierung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1a115-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="1a115-124">Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a115-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="1a115-125">Diese Eigenschaften werden in wmcodecdsp. h definiert.</span><span class="sxs-lookup"><span data-stu-id="1a115-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="1a115-126">Sie können diesen Modus explizit angeben, indem Sie die Eigenschaft [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf Variant \_ false festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a115-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="1a115-127">Weitere Informationen zum Festlegen von Eigenschaften für Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1a115-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="1a115-128">Wählen Sie die Codierungs Bitrate aus.</span><span class="sxs-lookup"><span data-stu-id="1a115-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="1a115-129">Bei der CBR-Codierung müssen Sie die Bitrate kennen, bei der der Stream codiert werden soll, bevor die Codierungs Sitzung beginnt.</span><span class="sxs-lookup"><span data-stu-id="1a115-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="1a115-130">Sie müssen die Bitrate während der Konfiguration des Encoders festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a115-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="1a115-131">Um dies zu erreichen, überprüfen Sie während der Durchführung einer Medientyp Aushandlung das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für audiodatenstreams) oder das " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) "-Attribut (für Videostreams) der verfügbaren Ausgabemedien Typen, und wählen Sie einen Ausgabe Medientyp aus, der der gewünschten Zielbitrate am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="1a115-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="1a115-132">Weitere Informationen finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1a115-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="1a115-133">Im folgenden Codebeispiel wird die Implementierung von setencodingproperties veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1a115-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="1a115-134">Diese Funktion legt Codierungs Eigenschaften auf Streamebene für CBR und VBR fest.</span><span class="sxs-lookup"><span data-stu-id="1a115-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="1a115-135">Einstellungen für "Leaky Bucket"</span><span class="sxs-lookup"><span data-stu-id="1a115-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="1a115-136">Bei der CBR-Codierung sind der durchschnittliche und der maximale Wert für den unzulässigen Bucket für den Datenstrom identisch.</span><span class="sxs-lookup"><span data-stu-id="1a115-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="1a115-137">Weitere Informationen zu diesen Parametern finden Sie [unter unkomplizierter Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="1a115-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="1a115-138">Zum Codieren von Audiodatenströmen müssen Sie die Werte für den Leaky-Bucket nach dem Aushandeln des Ausgabemedien Typs für den Encoder festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a115-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="1a115-139">Der Encoder berechnet das Puffer Fenster intern basierend auf der durchschnittlichen Bitrate, die für den Ausgabe Medientyp festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a115-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="1a115-140">Zum Festlegen von "Leaky Bucket"-Werten erstellen Sie ein Array von DWords, das die folgenden Werte in der Eigenschaft " [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) " im Eigenschaften Speicher der Medien Senke festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="1a115-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="1a115-141">Weitere Informationen finden Sie unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="1a115-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="1a115-142">Durchschnittliche Bitrate: Geben Sie die durchschnittliche Bitrate aus dem Ausgabe Medientyp an, der während der Medientyp Aushandlung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1a115-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="1a115-143">Verwenden Sie das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) ".</span><span class="sxs-lookup"><span data-stu-id="1a115-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="1a115-144">Puffer Fenster: Fragen Sie den Encoder nach der [**iwmcodecleakybucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) -Schnittstelle ab, und nennen Sie anschließend [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecigesichter. h, wmcodecdspuuid. lib).</span><span class="sxs-lookup"><span data-stu-id="1a115-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="1a115-145">Anfängliche Puffergröße: wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a115-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a115-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a115-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a115-147">ASF-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="1a115-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="1a115-148">Tutorial: 1-Pass-Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="1a115-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="1a115-149">Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="1a115-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
