---
description: Quality-Based Variablen-Bitrate-Codierung
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based Variablen-Bitrate-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348486"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="51fd2-103">Quality-Based Variablen-Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="51fd2-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="51fd2-104">Anders als bei der [Konstanten Bitrate-Codierung](constant-bit-rate-encoding.md) (CBR), bei der der Encoder versucht, eine bestimmte Bitrate des codierten Mediums beizubehalten, im variablenbitrate-Modus (VBR), versucht der Encoder, die bestmögliche Qualität der codierten Medien zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="51fd2-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="51fd2-105">Der primäre Unterschied zwischen CBR und VBR ist die Größe des verwendeten Puffer Fensters.</span><span class="sxs-lookup"><span data-stu-id="51fd2-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="51fd2-106">VBR-codierte Streams verfügen in der Regel über große Puffer Fenster im Vergleich zu CBR-codierten Streams.</span><span class="sxs-lookup"><span data-stu-id="51fd2-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="51fd2-107">Die Qualität des codierten Inhalts wird durch die Datenmenge bestimmt, die bei der Komprimierung des Inhalts verloren geht.</span><span class="sxs-lookup"><span data-stu-id="51fd2-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="51fd2-108">Viele Faktoren beeinflussen den Datenverlust im Komprimierungs Vorgang. Je komplexer die ursprünglichen Daten und die höhere Komprimierungs Quote, desto mehr Details gehen im Komprimierungs Vorgang jedoch verloren.</span><span class="sxs-lookup"><span data-stu-id="51fd2-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="51fd2-109">Im Qualitäts basierten VBR-Modus definieren Sie weder eine Bitrate noch ein Puffer Fenster, dem der Encoder folgen muss.</span><span class="sxs-lookup"><span data-stu-id="51fd2-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="51fd2-110">Stattdessen geben Sie eine Qualitätsstufe für einen digitalen Mediendaten Strom anstelle einer Bitrate an.</span><span class="sxs-lookup"><span data-stu-id="51fd2-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="51fd2-111">Der Encoder komprimiert den Inhalt, sodass alle Beispiele eine vergleichbare Qualität haben. Dadurch wird sichergestellt, dass die Qualität während der Wiedergabedauer konsistent ist, unabhängig von den Puffer Anforderungen des resultierenden Streams.</span><span class="sxs-lookup"><span data-stu-id="51fd2-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="51fd2-112">Bei der Qualitäts basierten VBR-Codierung werden häufig große komprimierte Datenströme erstellt.</span><span class="sxs-lookup"><span data-stu-id="51fd2-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="51fd2-113">Diese Art der Codierung eignet sich im Allgemeinen gut für die lokale Wiedergabe oder Netzwerkverbindungen mit hoher Bandbreite (bzw. herunterladen und wiedergeben).</span><span class="sxs-lookup"><span data-stu-id="51fd2-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="51fd2-114">Beispielsweise können Sie eine Anwendung schreiben, um Lieder aus CD in ASF-Dateien auf einem Computer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="51fd2-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="51fd2-115">Durch die Verwendung der Qualitäts basierten VBR-Codierung wird sichergestellt, dass alle kopierten Lieder dieselbe Qualität aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51fd2-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="51fd2-116">In diesen Fällen bietet die konsistente Qualität eine bessere Benutzer Leistung.</span><span class="sxs-lookup"><span data-stu-id="51fd2-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="51fd2-117">Der Nachteil der Qualitäts basierten VBR-Codierung besteht darin, dass es keine Möglichkeit gibt, die Größen-oder Bandbreitenanforderungen der codierten Medien vor der Codierungs Sitzung zu kennen, da der Encoder einen einzelnen Codierungs Durchlauf verwendet.</span><span class="sxs-lookup"><span data-stu-id="51fd2-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="51fd2-118">Dadurch können Qualitäts basierte VBR-codierte Dateien für Situationen ungeeignet werden, in denen der Arbeitsspeicher oder die Bandbreite eingeschränkt ist, z. b. die Wiedergabe von Inhalten auf tragbaren Medien und das Streaming über ein Netzwerk mit geringer Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="51fd2-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="51fd2-119">Konfigurieren des Encoders für Quality-Based VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="51fd2-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="51fd2-120">Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51fd2-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="51fd2-121">Diese Eigenschaften werden in wmcodecdsp. h definiert.</span><span class="sxs-lookup"><span data-stu-id="51fd2-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="51fd2-122">Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51fd2-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="51fd2-123">Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="51fd2-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="51fd2-124">In der folgenden Liste sind die Eigenschaften aufgeführt, die Sie für diesen Codierungstyp festlegen müssen:</span><span class="sxs-lookup"><span data-stu-id="51fd2-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="51fd2-125">Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft **mfpkey \_ vbrenabled** auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="51fd2-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="51fd2-126">Legen Sie den **verwendeten mfpkey- \_ passeswert** auf 1 fest, da dieser VBR-Modus einen Codierungs Durchlauf verwendet.</span><span class="sxs-lookup"><span data-stu-id="51fd2-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="51fd2-127">Legen Sie die gewünschte Qualitätsstufe (von 0 bis 100) fest, indem Sie die **\_ gewünschte \_ Eigenschaft "mfpkey** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="51fd2-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="51fd2-128">Der Qualitäts basierte VBR codiert den Inhalt nicht in vordefinierte Puffer Parameter.</span><span class="sxs-lookup"><span data-stu-id="51fd2-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="51fd2-129">Diese Qualitätsstufe, die für den gesamten Stream beibehalten wird, unabhängig von den Anforderungen an die Bitrate.</span><span class="sxs-lookup"><span data-stu-id="51fd2-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="51fd2-130">Legen Sie für Videostreams die durchschnittliche Bitrate auf einen Wert ungleich 0 (null) im Attribut " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) " für den Ausgabe Medientyp des Encoders fest.</span><span class="sxs-lookup"><span data-stu-id="51fd2-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="51fd2-131">Die genaue Bitrate wird nach Abschluss der Codierungs Sitzung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="51fd2-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="51fd2-132">Im folgenden Codebeispiel wird die Implementierung von setencodingproperties veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="51fd2-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="51fd2-133">Diese Funktion legt Codierungs Eigenschaften auf Streamebene für CBR und VBR fest.</span><span class="sxs-lookup"><span data-stu-id="51fd2-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="51fd2-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51fd2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51fd2-135">ASF-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="51fd2-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



