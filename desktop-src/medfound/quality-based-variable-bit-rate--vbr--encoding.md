---
description: Quality-Based Codierung variabler Bitraten
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based Codierung variabler Bitraten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19c2cd63d5bc6f777f702827e999cd9d2ae2a272194f4b776205c1581376256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722200"
---
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based Codierung variabler Bitraten

Im Gegensatz zur [Codierung konstanter Bitraten (Constant Bit Rate Encoding,](constant-bit-rate-encoding.md) CBR), bei der der Encoder eine bestimmte Bitrate der codierten Medien beibehalten möchte, versucht der Encoder im VBR-Modus (Variable Bit Rate), die bestmögliche Qualität der codierten Medien zu erreichen. Der Hauptunterschied zwischen CBR und VBR ist die Größe des verwendeten Pufferfensters. VBR-codierte Streams weisen im Vergleich zu CBR-codierten Streams in der Regel große Pufferfenster auf.

Die Qualität des codierten Inhalts wird durch die Menge der Daten bestimmt, die beim Komprimieren des Inhalts verloren geht. Viele Faktoren wirken sich auf den Datenverlust im Komprimierungsprozess aus. aber im Allgemeinen gilt: Je komplexer die ursprünglichen Daten und je höher das Komprimierungsverhältnis ist, desto mehr Details geht beim Komprimierungsprozess verloren.

Im qualitätsbasierten VBR-Modus definieren Sie keine Bitrate oder kein Pufferfenster, dem der Encoder folgen muss. Stattdessen geben Sie ein Qualitätsniveau für einen digitalen Medienstream anstelle einer Bitrate an. Der Encoder komprimiert den Inhalt, sodass alle Stichproben von vergleichbarer Qualität sind. Dadurch wird sichergestellt, dass die Qualität während der gesamten Wiedergabedauer konsistent ist, unabhängig von den Pufferanforderungen des resultierenden Streams.

Die qualitätsbasierte VBR-Codierung erstellt tendenziell große komprimierte Streams. Im Allgemeinen eignet sich diese Art der Codierung gut für die lokale Wiedergabe oder Netzwerkverbindungen mit hoher Bandbreite (oder herunterladen und wiedergeben). Beispielsweise können Sie eine Anwendung schreiben, um Titel von CD in ASF-Dateien auf einem Computer zu kopieren. Die Verwendung der qualitätsbasierten VBR-Codierung würde sicherstellen, dass alle kopierten Titel die gleiche Qualität aufweisen. In diesen Fällen bietet die konsistente Qualität eine bessere Benutzererfahrung.

Der Nachteil der qualitätsbasierten VBR-Codierung besteht darin, dass es tatsächlich keine Möglichkeit gibt, die Größen- oder Bandbreitenanforderungen der codierten Medien vor der Codierungssitzung zu kennen, da der Encoder einen einzelnen Codierungsdurchlauf verwendet. Dies kann qualitätsbasierte VBR-codierte Dateien für Situationen ungeeignet machen, in denen Arbeitsspeicher oder Bandbreite eingeschränkt sind, z. B. das Wiedergeben von Inhalten auf portablen Media Playern oder das Streaming über ein Netzwerk mit geringer Bandbreite.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Konfigurieren des Encoders für Quality-Based VBR-Codierung

Die Encoderkonfiguration wird über Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp.h definiert. Die Konfigurationseigenschaften müssen auf dem Encoder festgelegt werden, bevor der Ausgabemedientyp ausgehandelt wird. Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders.](configuring-the-encoder.md)

Die folgende Liste zeigt die Eigenschaften, die Sie für diesen Codierungstyp festlegen müssen:

-   Geben Sie den VBR-Codierungsmodus an, indem Sie die **MFPKEY \_ VBRENABLED-Eigenschaft** auf VARIANT \_ TRUE festlegen.
-   Legen Sie **MFPKEY \_ PASSESUSED** auf 1 fest, da dieser VBR-Modus einen Codierungsdurchlauf verwendet.
-   Legen Sie den gewünschten Qualitätsgrad (von 0 bis 100) fest, indem Sie die **MFPKEY \_ DESIRED \_ VBRQUALITY-Eigenschaft** festlegen. Qualitätsbasierte VBR codiert den Inhalt nicht in vordefinierte Pufferparameter. Diese Qualitätsstufe, die für den gesamten Stream beibehalten wird, unabhängig von den resultierenden Bitratenanforderungen.
-   Legen Sie für Videostreams die durchschnittliche Bitrate auf einen Wert ungleich 0 (null) im [**MF \_ MT \_ AVG \_ BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) für den Ausgabemedientyp des Encoders fest. Die genaue Bitrate wird aktualisiert, nachdem die Codierungssitzung abgeschlossen ist.

Das folgende Codebeispiel zeigt die Implementierung für SetEncodingProperties. Diese Funktion legt Codierungseigenschaften auf Streamebene für CBR und VBR fest.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Codierungstypen](asf-encoding-types.md)
</dt> </dl>

 

 



