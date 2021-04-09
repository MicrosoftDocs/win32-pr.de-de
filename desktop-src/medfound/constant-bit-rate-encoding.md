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
# <a name="constant-bit-rate-encoding"></a>Konstante Bitrate-Codierung

Bei der Codierung mit konstanter Bitrate (CBR) kennt der Encoder die Bitrate der Ausgabemedien Beispiele und das Puffer Fenster ("Leaky Bucket Parameters"), bevor die Codierungs Sitzung beginnt. Der Encoder verwendet die gleiche Anzahl von Bits, um jede Sekunde von Sample während der gesamten Dauer der Datei zu codieren, um die Zielbitrate für einen Datenstrom zu erzielen. Dies schränkt die Variation der Größe der streambeispiele ein. Außerdem liegt die Bitrate während der Codierungs Sitzung nicht genau beim angegebenen Wert, sondern bleibt in der Nähe der Zielbitrate.

CBR-Codierung ist hilfreich, wenn Sie die Bitrate oder die geschätzte Dauer einer Datei herausfinden möchten, ohne die gesamte Datei zu analysieren. Dies wird z. B. beim Livestreaming benötigt, wenn die Medieninhalte mit einer vorhersehbaren Bitrate und mit konstanter Bandbreitennutzung gestreamt werden müssen.

Der Nachteil der CBR-Codierung besteht darin, dass die Qualität des codierten Inhalts nicht konstant ist. Da es schwieriger ist, Inhalte zu komprimieren, sind Teile eines CBR-Streams von geringerer Qualität als andere. Ein typischer Film hat z. b. einige Szenen, die relativ statisch sind, und einige Szenen, die vollständig ausgeführt werden. Wenn Sie einen Film mit CBR codieren, sind die Szenen, die statisch und somit leicht zu codieren sind, von höherer Qualität als die Aktions Szenen, die für die Beibehaltung der gleichen Qualität eine höhere Stichprobengröße erfordern.

Im Allgemeinen sind Variationen der Qualität einer CBR-Datei in niedrigeren Bitraten deutlicher ausgeprägt. Bei höheren Bitraten variiert die Qualität einer CBR-codierten Datei weiterhin, aber die Qualitätsprobleme sind für den Benutzer weniger bemerkbar. Wenn Sie die CBR-Codierung verwenden, sollten Sie die Bandbreite so hoch festlegen, dass Sie das Liefer Szenario zulässt.

-   [CBR-Konfigurationseinstellungen](#cbr-configuration-settings)
-   [Einstellungen für "Leaky Bucket"](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a>CBR-Konfigurationseinstellungen

Sie müssen einen Encoder konfigurieren, indem Sie den Codierungstyp und die verschiedenen streamspezifischen Einstellungen vor der Codierungs Sitzung angeben.

**So konfigurieren Sie den Encoder für die CBR-Codierung**

1.  Geben Sie den CBR-Codierungs Modus an.

    Standardmäßig ist der Encoder für die Verwendung der CBR-Codierung konfiguriert. Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp. h definiert. Sie können diesen Modus explizit angeben, indem Sie die Eigenschaft [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf Variant \_ false festlegen. Weitere Informationen zum Festlegen von Eigenschaften für Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).

2.  Wählen Sie die Codierungs Bitrate aus.

    Bei der CBR-Codierung müssen Sie die Bitrate kennen, bei der der Stream codiert werden soll, bevor die Codierungs Sitzung beginnt. Sie müssen die Bitrate während der Konfiguration des Encoders festlegen. Um dies zu erreichen, überprüfen Sie während der Durchführung einer Medientyp Aushandlung das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für audiodatenstreams) oder das " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) "-Attribut (für Videostreams) der verfügbaren Ausgabemedien Typen, und wählen Sie einen Ausgabe Medientyp aus, der der gewünschten Zielbitrate am nächsten liegt. Weitere Informationen finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).

Im folgenden Codebeispiel wird die Implementierung von setencodingproperties veranschaulicht. Diese Funktion legt Codierungs Eigenschaften auf Streamebene für CBR und VBR fest.


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



### <a name="leaky-bucket-settings"></a>Einstellungen für "Leaky Bucket"

Bei der CBR-Codierung sind der durchschnittliche und der maximale Wert für den unzulässigen Bucket für den Datenstrom identisch. Weitere Informationen zu diesen Parametern finden Sie [unter unkomplizierter Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).

Zum Codieren von Audiodatenströmen müssen Sie die Werte für den Leaky-Bucket nach dem Aushandeln des Ausgabemedien Typs für den Encoder festlegen. Der Encoder berechnet das Puffer Fenster intern basierend auf der durchschnittlichen Bitrate, die für den Ausgabe Medientyp festgelegt wurde.

Zum Festlegen von "Leaky Bucket"-Werten erstellen Sie ein Array von DWords, das die folgenden Werte in der Eigenschaft " [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) " im Eigenschaften Speicher der Medien Senke festlegen kann. Weitere Informationen finden Sie unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).

-   Durchschnittliche Bitrate: Geben Sie die durchschnittliche Bitrate aus dem Ausgabe Medientyp an, der während der Medientyp Aushandlung ausgewählt wird. Verwenden Sie das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) ".
-   Puffer Fenster: Fragen Sie den Encoder nach der [**iwmcodecleakybucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) -Schnittstelle ab, und nennen Sie anschließend [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecigesichter. h, wmcodecdspuuid. lib).
-   Anfängliche Puffergröße: wird auf 0 festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Codierungs Typen](asf-encoding-types.md)
</dt> <dt>

[Tutorial: 1-Pass-Windows-Medien Codierung](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
