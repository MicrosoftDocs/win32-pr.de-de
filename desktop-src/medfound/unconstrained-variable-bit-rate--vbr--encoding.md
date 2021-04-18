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
# <a name="unconstrained-variable-bit-rate-encoding"></a>Unbeschränkte Variablen Bitrate-Codierung

Im uneingeschränkten VBR-Codierungs Modus wird der Inhalt in die höchste mögliche Qualität codiert, während eine angegebene Bitrate beibehalten wird.

Bei der uneingeschränkten VBR-Codierung werden zwei Codierungs Durchgänge verwendet. Wenn Sie die unbeschränkte VBR-Codierung verwenden, geben Sie eine Bitrate für den Stream an, wie bei [konstanter Bitrate-Codierung](constant-bit-rate-encoding.md). Der Encoder verwendet diesen Wert jedoch nur als durchschnittliche Bitrate für den Stream und codiert, sodass die Qualität so hoch wie möglich ist, während der Durchschnitt beibehalten wird. Die einzelnen vom Encoder erstellten Beispiele variieren in der Größe ohne explizite Puffer Limits. Die durchschnittliche Bitrate während der Codierungs Sitzung und die Dauer des Streams dürfen jedoch nicht größer sein als der von Ihnen angegebene Wert. Die tatsächliche Bitrate an einem beliebigen Punkt im codierten Stream kann stark vom Durchschnittswert abweichen. Sie legen kein Puffer Fenster für die nicht eingeschränkte VBR-Codierung fest. Stattdessen berechnet der Encoder die Größe des erforderlichen Puffer Fensters basierend auf den Anforderungen der codierten Stichproben. Dies bedeutet, dass es keine Beschränkung auf die Größe der einzelnen Stichproben im Stream gibt, solange die durchschnittliche Bitrate kleiner oder gleich dem Wert ist, den Sie festgelegt haben.

Der Vorteil der uneingeschränkten VBR-Codierung besteht darin, dass der komprimierte Datenstrom die höchste mögliche Qualität aufweist und gleichzeitig in einer vorhersagbaren durchschnittlichen Bandbreite bleibt. Verwenden Sie diese Anwendung, wenn Sie eine Bandbreite angeben müssen, aber Schwankungen in Bezug auf die angegebene Bandbreite zulässig sind. beispielsweise für lokale Dateien oder nur für das herunterladen.

Der Nachteil dieses Codierungs Modus besteht darin, dass der Encoder das Puffer Fenster auf einen beliebigen Wert festlegen kann, der nach der Codierung erforderlich ist, sodass Sie keine Kontrolle über die Puffergröße haben. In den meisten Fällen sollten Sie, wenn Sie sich keine Gedanken über die Größe des Puffers oder die Konsistenz der Bandbreitennutzung machen, die [Qualitäts basierte variierungsbitrate-Codierung](quality-based-variable-bit-rate--vbr--encoding.md) verwenden.

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Konfigurieren des Encoders für nicht eingeschränkten VBR

Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp. h definiert. Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden. Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md). Basierend auf den angegebenen Eigenschafts Werten können Sie die unterstützten VBR-Ausgabetypen auflisten und die erforderliche auf der Grundlage der durchschnittlichen Bitrate auf der Grundlage des Encoders [Media Foundation Transform](media-foundation-transforms.md) (MFT) auswählen.

In der folgenden Liste sind die Eigenschaften aufgeführt, die Sie für diesen Codierungstyp festlegen müssen:

-   Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft mfpkey \_ vbrenabled auf Variant \_ true festlegen.
-   Legen Sie die verwendete mfpkey-Kennung \_ auf 2 fest, da der nicht eingeschränkte VBR-Modus zwei Codierungs Durchläufen verwendet.
-   Überprüfen Sie beim Auflisten des Ausgabemedien Typs das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für Audiostreams) oder das Attribut " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) " (für Videostreams) der verfügbaren Ausgabemedien Typen. Wählen Sie einen Ausgabe Medientyp aus, bei dem die durchschnittliche Bitrate der gewünschten durchschnittlichen Bitrate liegt, die der Encoder im codierten Inhalt behalten soll. Weitere Informationen zum Auswählen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).

Um den Puffer Fenster Wert durch den Encoder festzulegen, nennen Sie **iwmcodecleakybucket:: getbuffersizebits**, das in wmcodecigesichter. h und wmcodecdspuuid. lib definiert ist, nach der Codierungs Sitzung. Zum Hinzufügen der Unterstützung für nicht eingeschränkte VBR-Datenströme müssen Sie diesen Wert im Attribut " [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) " (durchschnittliche Anzahl der unbeschränkten Bucket-Werte) für das Datenstrom-Konfigurationsobjekt festlegen, während Sie das ASF-Profil konfigurieren.

Im folgenden Beispiel wird die setencodingtype-Methode der Beispiel Klasse cencoder geändert, um den nicht eingeschränkten VBR-Modus einzurichten. Weitere Informationen zu dieser Klasse finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md). Informationen zu den in diesem Beispiel verwendeten Hilfsmakros finden Sie unter Verwenden der Media Foundation-Code Beispiele.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Codierungs Typen](asf-encoding-types.md)
</dt> <dt>

[Das Leaky Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Erstellen einer Topologie für Two-Pass Windows-Medien Codierung](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



