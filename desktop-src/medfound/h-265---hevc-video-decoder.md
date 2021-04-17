---
description: Der Video Decoder Media Foundation H. 265 ist eine Media Foundation Transformation, die das Decodieren von H. 265/hevc-Inhalten im Anhang B-Format unterstützt und für die Wiedergabe von MP4-und M2TS-Dateien verwendet werden kann.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: H. 265/hevc-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527698"
---
# <a name="h265--hevc-video-decoder"></a>H. 265/hevc-Video Decoder

Der Video Decoder Media Foundation H. 265 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das Decodieren von H. 265/hevc-Inhalten im Anhang B-Format unterstützt und für die Wiedergabe von MP4-und M2TS-Dateien verwendet werden kann.

Der H. 265-Video Decoder macht die folgenden Schnittstellen verfügbar.

-   [**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) (unterstützt in Windows 8)
-   [**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**Imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Um eine Instanz des Decoders zu erstellen, rufen Sie die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion auf.

## <a name="input-types"></a>Eingabetypen

Der Eingabetyp muss mindestens die beiden folgenden Attribute enthalten:



| Attribut                                                 | BESCHREIBUNG                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | **MF MediaType- \_ Video**                                                                        |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)        | [MF-Format \_ Hevc oder](video-subtype-guids.md) MF-Format \_ hevc \_ es |



 

Der erste Medien Untertyp, MF Videoformat \_ hevc, gibt an, dass die Medien Beispiele den H. 265-Bitstrom mit Start Codes enthalten und der Stream überlappende SPS/PPS verfügt. Es wird von einem Frame pro Stichprobe ausgegangen.

Der Medien Untertyp mfvideoformat \_ hevc \_ es gibt an, dass die Medien Beispiele einen elementaren H. 265-Bitstream enthalten, wobei jedes Beispiel ein partielles Bild, mehrere Bilder, einige Bilder und ein partielles Bild enthalten kann.

Die Eingabemedien Typen können sich nicht dynamisch zwischen zwei Typen ändern. Der Decoder kann in-Flight-Ausgabeformat Änderungen auf der Grundlage der elementaren Datenstrom Syntax (Seitenverhältnis, Dimension, damit-Flags, farbige metrieinformationen) erkennen und entsprechende Änderungen des Ausgabemedien Typs auslöst.

Für den Eingabe Medientyp erwartet der Decoder, dass die Quelle das korrekte Profil festgelegt hat. Wenn der Inhalt beispielsweise 10bit sein wird, sollte der Eingabe Medientyp das Profil als Main10 angeben.

## <a name="output-types"></a>Ausgabetypen

Der Decoder unterstützt die folgenden Ausgabe Untertypen:

-   **MF-Format \_ NV12**
-   **MF-Format \_ P010**

Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="transform-attributes"></a>Transformations Attribute

Der H. 265-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.



| Attribut                                                                                       | BESCHREIBUNG                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md)                                     | Aktiviert oder deaktiviert den Decodierungs Modus mit niedriger Latenz.                                                                                |
| [Codecapi \_ avdecnumworkerthreads](codecapi-avdecnumworkerthreads.md)                           | Legt die Anzahl von Arbeitsthreads fest, die vom Decoder verwendet werden.                                                                        |
| [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.                                                                                |
| [Länge der MF- \_ Nalu- \_ Länge \_](mf-nalu-length-set.md)                                                 | Gibt an, dass Nalu-Längen Informationen als BLOB mit jedem komprimierten H. 265-Beispiel gesendet werden.                              |
| [Informationen zur Länge der MF- \_ Nalu \_ \_](mf-nalu-length-information.md)                                 | Gibt die Länge von nalus in der Stichprobe an. Hierbei handelt es sich um ein MF-BLOB, das auf komprimierte Eingabe Beispiele für den H. 265-Decoder festgelegt ist. |
| [\_Anzahl der \_ minimalen \_ Ausgabe \_ Beispiele \_ für MF-SA](mf-sa-minimum-output-sample-count.md)                 | Gibt die maximale Anzahl von Ausgabe Beispielen an.                                                                               |



 

Der H. 265-Decoder unterstützt die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle. Diese Schnittstelle bietet eine alternativate-API zum Festlegen der folgenden Codec-Eigenschaften.

-   [Codecapi \_ avdecnumworkerthreads](codecapi-avdecnumworkerthreads.md)
-   [Codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [Codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Format Einschränkungen

Der Decoder unterstützt die folgenden Formate:



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profile/Ebenen    | Haupt-, Haupt Bild-und Main10-profile                                                                                                                                                                                                                        |
| Chroma-Formate     | 4:2:0 Chroma                                                                                                                                                                                                                                                         |
| Minimale Auflösung | 48 × 48 Pixel                                                                                                                                                                                                                                                       |
| Maximale Auflösung | 4096 × 2304 Pixel<br/> Die maximale garantierte Auflösung der DXVA-Beschleunigung beträgt 1920 × 1088 Pixel. bei höherer Auflösung erfolgt die Decodierung mit DXVA, wenn Sie von der zugrunde liegenden Hardware unterstützt wird. andernfalls erfolgt die Decodierung mit Software.<br/> |
| DXVA               | Der Decoder unterstützt DX11 und DX12 DXVA, aber nicht DXVA Version 2 oder DXVA Version 1.                                                                                                                                                                                                         |



 

Eingabedaten müssen dem Anhang B des ITU-T H. 265 \| ISO/IEC 23008-2 entsprechen. Die Daten müssen die Start Codes enthalten. Der Decoder überspringt bytes, bis ein gültiger Sequenz Parametersatz (SPS) und ein Bildparameter Satz (PPS) im Bytestream gefunden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
