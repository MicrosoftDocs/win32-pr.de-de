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
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained Variablen-Bitrate-Codierung

In der Spitzen eingeschränkten Variablen Bitrate (VBR) wird der Inhalt in eine angegebene Bitrate und *Spitzenwerte* codiert: eine Spitzen Bitrate und ein Spitzen Puffer Fenster. Diese Spitzenwerte werden auch als *Maximale Lecky-Bucket-Werte* bezeichnet. Die Datei wird so codiert, dass Sie einem Puffer entspricht, der durch die Spitzenwerte beschrieben wird, sodass die durchschnittliche Bitrate des Streams kleiner oder kleiner als der Wert für die durchschnittliche Bitrate ist, den Sie angegeben haben.

In der Regel ist die Spitzen Bitrate sehr hoch. Der Encoder stellt sicher, dass der angegebene Wert für die durchschnittliche Bitrate für die Dauer des Streams beibehalten wird (durchschnittliche Bitrate >= (gesamte Streamgröße in Bits/Stream-Dauer in Sekunden)). Sehen Sie sich das folgende Beispiel an: Sie konfigurieren einen Stream mit einer durchschnittlichen Bitrate von 16.000 Bits pro Sekunde, einer Spitzen Bitrate von 48.000 Bits pro Sekunde und einem Spitzen Puffer Fenster von 3.000 (3 Sekunden). Die Größe des für den Stream verwendeten Puffers beträgt 144.000 Bits (48.000 Bits pro Sekunde \* 3 Sekunden), wie durch die Spitzenwerte festgelegt. Der Encoder komprimiert die Daten, damit Sie diesem Puffer entsprechen. Außerdem muss die durchschnittliche Bitrate des Streams 16.000 oder weniger betragen. Wenn der Encoder große Beispiele zum Verarbeiten eines komplexen Inhalts Segments erstellen muss, kann er die große Puffergröße nutzen. Andere Teile des Streams müssen jedoch mit einer niedrigeren Bitrate codiert werden, um den Durchschnitt auf die angegebene Ebene zu verringern. Die mit Spitzen Beschränkung beschränkte VBR-Codierung eignet sich für die Wiedergabe von Geräten mit einer begrenzten Pufferkapazität und Datenraten Einschränkungen. Ein gängiges Beispiel hierfür ist die Codierung, die für DVDs verwendet wird, wenn die Decodierung von einem Chip in einem Gerät durchgeführt wird, bei dem Hardware Einschränkungen beachtet werden müssen.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Konfigurieren des Encoders für Peak-Constrained VBR

VBR mit hoher Einschränkung ist so ähnlich wie der eingeschränkte [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) , da es sich auf eine durchschnittliche Bitrate während der Dauer des Streams beschränkt. Darüber hinaus entspricht VBR mit hoher Einschränkung einem Spitzen Puffer. Dieser Puffer wird mit einer Spitzen Bitrate und einem Spitzen Puffer Fenster beschrieben. Dieser Modus verwendet zwei Codierungs Durchläufen und bietet dem Encoder Flexibilität bei der Codierung einzelner Stichproben, während die Spitzen Grenzen einhalten.

Die Encoderkonfiguration wird durch Eigenschaftswerte festgelegt. Diese Eigenschaften werden in wmcodecdsp. h definiert. Vor dem Aushandeln des Ausgabemedien Typs müssen die Konfigurations Eigenschaften für den Encoder festgelegt werden. Weitere Informationen zum Festlegen von Eigenschaften für den Encoder finden Sie unter [Konfigurieren des Encoders](configuring-the-encoder.md). Basierend auf den angegebenen Eigenschafts Werten können Sie die unterstützten VBR-Ausgabetypen auflisten und die erforderliche auf der Grundlage der durchschnittlichen Bitrate auf der Grundlage des Encoders [Media Foundation Transform](media-foundation-transforms.md) (MFT) auswählen.

Sie müssen die folgenden Eigenschaften für diese Art von Codierung festlegen:

-   Legen Sie den VBR-Codierungs Modus fest, indem Sie die Eigenschaft mfpkey \_ vbrenabled auf Variant \_ true festlegen.
-   Legen Sie den Wert für "mfpkey" auf "2" fest \_ , da der Modus mit hoher eingeschränkter Verwendung zwei Codierungs Durchläufen verwendet.
-   Legen Sie mfpkey \_ Rmax fest, um die maximale Bitrate anzugeben, und legen Sie mfpkey \_ bmax fest, um das Spitzen Puffer Fenster anzugeben.
-   Überprüfen Sie beim Auflisten des Ausgabemedien Typs das Attribut " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) " (für audiodatenstreams) oder das " [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) "-Attribut (für Videostreams) der verfügbaren Ausgabemedien Typen, und wählen Sie einen Ausgabe Medientyp aus, der der durchschnittlichen Bitrate am nächsten liegt, die der Encoder im codierten Inhalt behalten soll Weitere Informationen zum Auswählen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Es wird empfohlen, die Spitzen Bitrate auf mindestens doppelte die durchschnittliche Bitrate festzulegen. Wenn die Spitzen Rate auf einen niedrigeren Wert festgelegt wird, codiert der Encoder den Inhalt möglicherweise als zwei-Pass-CBR anstelle von VBR mit eingeschränkter Spitzen Zahl.

 

Um den vom Encoder festgelegten Puffer Fenster Wert abzurufen, nennen Sie nach der Codierungs Sitzung **iwmcodecleakybucket:: getbuffersizebits**, das in wmcodecigesichter. h, wmcodecdspuuid. lib, definiert ist. Zum Hinzufügen der Unterstützung für nicht eingeschränkte VBR-Datenströme müssen Sie diesen Wert im " [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) "-Attribut (maximale Anzahl von unbeschränkten Bucket-Werten) für das Datenstrom-Konfigurationsobjekt festlegen, während Sie das ASF-Profil konfigurieren.

Im folgenden Codebeispiel wird die setencodingtype-Methode der Beispiel Klasse cencoder geändert, um den VBR-Modus mit hoher Auslastung einzurichten. Weitere Informationen zu dieser Klasse finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md). Informationen zu den in diesem Beispiel verwendeten Hilfsmakros finden Sie unter Verwenden der Media Foundation-Code Beispiele.


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

[ASF-Codierungs Typen](asf-encoding-types.md)
</dt> <dt>

[Das Leaky Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Erstellen einer Topologie für Two-Pass Windows-Medien Codierung](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



