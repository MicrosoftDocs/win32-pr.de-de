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
# <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based Variablen-Bitrate-Codierung

Anders als bei der [Konstanten Bitrate-Codierung](constant-bit-rate-encoding.md) (CBR), bei der der Encoder versucht, eine bestimmte Bitrate des codierten Mediums beizubehalten, im variablenbitrate-Modus (VBR), versucht der Encoder, die bestmögliche Qualität der codierten Medien zu erzielen. Der primäre Unterschied zwischen CBR und VBR ist die Größe des verwendeten Puffer Fensters. VBR-codierte Streams verfügen in der Regel über große Puffer Fenster im Vergleich zu CBR-codierten Streams.

Die Qualität des codierten Inhalts wird durch die Datenmenge bestimmt, die bei der Komprimierung des Inhalts verloren geht. Viele Faktoren beeinflussen den Datenverlust im Komprimierungs Vorgang. Je komplexer die ursprünglichen Daten und die höhere Komprimierungs Quote, desto mehr Details gehen im Komprimierungs Vorgang jedoch verloren.

Im Qualitäts basierten VBR-Modus definieren Sie weder eine Bitrate noch ein Puffer Fenster, dem der Encoder folgen muss. Stattdessen geben Sie eine Qualitätsstufe für einen digitalen Mediendaten Strom anstelle einer Bitrate an. Der Encoder komprimiert den Inhalt, sodass alle Beispiele eine vergleichbare Qualität haben. Dadurch wird sichergestellt, dass die Qualität während der Wiedergabedauer konsistent ist, unabhängig von den Puffer Anforderungen des resultierenden Streams.

Bei der Qualitäts basierten VBR-Codierung werden häufig große komprimierte Datenströme erstellt. Diese Art der Codierung eignet sich im Allgemeinen gut für die lokale Wiedergabe oder Netzwerkverbindungen mit hoher Bandbreite (bzw. herunterladen und wiedergeben). Beispielsweise können Sie eine Anwendung schreiben, um Lieder aus CD in ASF-Dateien auf einem Computer zu kopieren. Durch die Verwendung der Qualitäts basierten VBR-Codierung wird sichergestellt, dass alle kopierten Lieder dieselbe Qualität aufweisen. In diesen Fällen bietet die konsistente Qualität eine bessere Benutzer Leistung.

Der Nachteil der Qualitäts basierten VBR-Codierung besteht darin, dass es keine Möglichkeit gibt, die Größen-oder Bandbreitenanforderungen der codierten Medien vor der Codierungs Sitzung zu kennen, da der Encoder einen einzelnen Codierungs Durchlauf verwendet. Dadurch können Qualitäts basierte VBR-codierte Dateien für Situationen ungeeignet werden, in denen der Arbeitsspeicher oder die Bandbreite eingeschränkt ist, z. b. die Wiedergabe von Inhalten auf tragbaren Medien und das Streaming über ein Netzwerk mit geringer Bandbreite.

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a>Konfigurieren des Encoders für Quality-Based VBR-Codierung

Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp. h definiert. Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden. Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md).

In der folgenden Liste sind die Eigenschaften aufgeführt, die Sie für diesen Codierungstyp festlegen müssen:

-   Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft **mfpkey \_ vbrenabled** auf Variant \_ true festlegen.
-   Legen Sie den **verwendeten mfpkey- \_ passeswert** auf 1 fest, da dieser VBR-Modus einen Codierungs Durchlauf verwendet.
-   Legen Sie die gewünschte Qualitätsstufe (von 0 bis 100) fest, indem Sie die **\_ gewünschte \_ Eigenschaft "mfpkey** " festlegen. Der Qualitäts basierte VBR codiert den Inhalt nicht in vordefinierte Puffer Parameter. Diese Qualitätsstufe, die für den gesamten Stream beibehalten wird, unabhängig von den Anforderungen an die Bitrate.
-   Legen Sie für Videostreams die durchschnittliche Bitrate auf einen Wert ungleich 0 (null) im Attribut " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) " für den Ausgabe Medientyp des Encoders fest. Die genaue Bitrate wird nach Abschluss der Codierungs Sitzung aktualisiert.

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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Codierungs Typen](asf-encoding-types.md)
</dt> </dl>

 

 



