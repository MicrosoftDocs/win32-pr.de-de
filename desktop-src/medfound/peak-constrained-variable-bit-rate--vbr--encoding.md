---
description: 'In der variablen Bitrate mit Spitzenbeschränkung (Peak-Constrained Variable Bit Rate, VBR) wird der Inhalt mit einer angegebenen Bitrate und Spitzenwerten codiert: einer Spitzenbitrate und einem Spitzenpufferfenster.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained variable Bitratencodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97361c6d4ac8cefd33b223157347e450252691cab024e167862f50c7aac0fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737667"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained variable Bitratencodierung

In der variablen Bitrate mit Spitzenbeschränkung (Peak-Constrained Variable Bit Rate, VBR) wird der Inhalt mit einer angegebenen Bitrate und Spitzenwerten codiert: einer Spitzenbitrate und einem Spitzenpufferfenster. Diese Spitzenwerte werden auch als *Bucketwerte mit Spitzenverlust bezeichnet.* Die Datei wird so codiert, dass sie einem Puffer entspricht, der durch die Spitzenwerte beschrieben wird, damit die durchschnittliche Gesamtbitrate des Streams gleich oder kleiner als der von Ihnen angegebene Wert für die durchschnittliche Bitrate ist.

In der Regel ist die Spitzenbitrate recht hoch. Der Encoder stellt sicher, dass der angegebene Wert für die durchschnittliche Bitrate über die Dauer des Streams beibehalten wird (durchschnittliche Bitrate >= (Gesamtstromgröße in Bits/Streamdauer in Sekunden)). Betrachten Sie das folgende Beispiel: Sie konfigurieren einen Stream mit einer durchschnittlichen Bitrate von 16.000 Bits pro Sekunde, einer Spitzenbitrate von 48.000 Bits pro Sekunde und einem Spitzenpufferfenster von 3.000 (3 Sekunden). Der für den Stream verwendete Puffer beträgt 144.000 Bits (48.000 Bits pro Sekunde 3 Sekunden), wie durch die Spitzenwerte \* festgelegt. Der Encoder komprimiert die Daten so, dass sie diesem Puffer entsprechen. Darüber hinaus muss die durchschnittliche Bitrate des Streams 16.000 oder weniger sein. Wenn der Encoder große Stichproben erstellen muss, um ein komplexes Inhaltssegment zu verarbeiten, kann er die große Puffergröße nutzen. Andere Teile des Streams müssen jedoch mit einer niedrigeren Bitrate codiert werden, um den Durchschnitt auf die angegebene Ebene zu senken. Die VBR-Codierung mit Spitzeneinschränkung ist nützlich für Wiedergabegeräte mit begrenzten Pufferkapazitäts- und Datenrateneinschränkungen. Ein gängiges Beispiel hierfür ist die Codierung, die für DVDs verwendet wird, wenn die Decodierung von einem Chip auf einem Gerät durchgeführt wird, bei dem Hardwareeinschränkungen berücksichtigt werden müssen.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Konfigurieren des Encoders für Peak-Constrained VBR

Die VBR mit Eingeschränkter Spitzenlast ist wie eine nicht schränkte [VBR,](unconstrained-variable-bit-rate--vbr--encoding.md) da sie auf eine durchschnittliche Bitrate über die Dauer des Streams beschränkt ist. Darüber hinaus entspricht die VBR mit Eingeschränkter Spitzenlast einem Spitzenpuffer. Dieser Puffer wird mithilfe einer Spitzenbitrate und eines Spitzenpufferfensters beschrieben. Dieser Modus verwendet zwei Codierungsüberläufe und bietet dem Encoder Flexibilität bei der Codierung einzelner Stichproben unter Einhaltung der Spitzeneinschränkungen.

Die Encoderkonfiguration wird über Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp.h definiert. Die Konfigurationseigenschaften müssen für den Encoder festgelegt werden, bevor der Ausgabemedientyp aushandelt wird. Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md). Basierend auf den angegebenen Eigenschaftswerten können Sie die unterstützten VBR-Ausgabetypen aufzählen und basierend auf der durchschnittlichen Bitrate den erforderlichen für den Encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) auswählen.

Sie müssen die folgenden Eigenschaften für diesen Codierungstyp festlegen:

-   Geben Sie den VBR-Codierungsmodus an, indem Sie die Eigenschaft MFPKEY \_ VBRENABLED auf VARIANT \_ TRUE festlegen.
-   Legen Sie MFPKEY PASSESUSED auf 2 fest, da der VBR-Modus mit Spitzenbeschränkung \_ zwei Codierungsüberläufe verwendet.
-   Legen Sie MFPKEY \_ RMAX fest, um die Spitzenbitrate anzugeben, und legen Sie MFPKEY BMAX fest, \_ um das Spitzenpufferfenster anzugeben.
-   Überprüfen Sie beim Aufzählen des Ausgabemedientyps das [**MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut**](mf-mt-audio-avg-bytes-per-second-attribute.md) (für Audiostreams) oder das [**MF MT \_ \_ AVG \_ BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) (für Videostreams) der verfügbaren Ausgabemedientypen, und wählen Sie einen Ausgabemedientyp aus, der die durchschnittliche Bitrate hat, die der gewünschten durchschnittlichen Bitrate am nächsten kommt, die der Encoder im codierten Inhalt verwalten soll. Weitere Informationen zum Auswählen des Ausgabemedientyps finden Sie unter [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Es wird empfohlen, die Spitzenbitrate auf mindestens das Doppelte der durchschnittlichen Bitrate zu setzen. Das Festlegen der Spitzenrate auf einen niedrigeren Wert kann dazu führen, dass der Encoder den Inhalt als ZWEI-Durchgang-CBR statt als VBR mit Eingeschränkter Spitzenlast codiert.

 

Um den vom Encoder festgelegten Pufferfensterwert zu erhalten, rufen Sie **IWMCodecLeakyBucket::GetBufferSizeBits**, definiert in wmcodecifaces.h, wmcodecdspuuid.lib, nach der Codierungssitzung auf. Um die constrained VBR-Unterstützung für die Streams hinzuzufügen, müssen Sie diesen Wert im [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2-Attribut**](mf-asfstreamconfig-leakybucket2-attribute.md) (Bucketwerte mit Spitzenverlust) für das Streamkonfigurationsobjekt festlegen, während Sie das ASF-Profil konfigurieren.

Im folgenden Codebeispiel wird die SetEncodingType-Methode der CEncoder-Beispielklasse so modifiziert, dass der VBR-Modus mit Eingeschränkter Spitzenlast eingerichtet wird. Informationen zu dieser Klasse finden Sie unter [Encoder-Beispielcode](encoder-example-code.md). Informationen zu den in diesem Beispiel verwendeten Hilfsmakros finden Sie unter Verwenden der Media Foundation Codebeispiele.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Codierungstypen](asf-encoding-types.md)
</dt> <dt>

[Das Leaky Bucket Buffer-Modell](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Erstellen einer Topologie für die Two-Pass Windows Mediencodierung](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



