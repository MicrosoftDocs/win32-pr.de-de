---
description: Der MPEG-2-Videodecoder ist eine Media Foundation-Transformation, die MPEG-1- und MPEG-2-Videos decodiert.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: MPEG-2-Videodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e2b270cadb114875fb63bc6c57ce2ddd63eecb2815b8fe3bcee175710d1771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012590"
---
# <a name="mpeg-2-video-decoder"></a>MPEG-2-Videodecoder

Der MPEG-2-Videodecoder ist eine [Media Foundation-Transformation,](media-foundation-transforms.md) die MPEG-1- und MPEG-2-Videos decodiert. Der Decoder unterstützt MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) und MPEG-1 video (ISO/IEC 11172-2).

## <a name="input-types"></a>Eingabetypen

Der Decoder unterstützt die folgenden Eingabemedientypen.

| attribute                                                 | BESCHREIBUNG                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md) | **\_MFMediaType-Video**                                                  |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Ausgabetypen

Der Decoder unterstützt die folgenden Ausgabetypen.

| attribute                                                 | BESCHREIBUNG                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md) | **\_MFMediaType-Video**                                                                                                                                                         |
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Hinweise

Der MPEG-2-Videodecoder macht die folgenden Schnittstellen verfügbar:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**HAPQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**HAPQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**THICKNESSRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**1000000000**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**VERALTENRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Die Eingabe für den Decoder muss ein elementarer Stream sein. Die maximal unterstützte Auflösung beträgt 1920 × 1.088 Pixel.

Der Decoder unterstützt DirectX Video Acceleration (DXVA) mit Microsoft Direct3D 9 oder Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Spezielle Decodierungsmodi

-   **Modus mit geringer Latenz.** Dieser Modus eignet sich für Szenarien wie Echtzeitkommunikation. Dadurch wird die Startlatenz reduziert, sodass der Decoder früher das erste Ausgabebeispiel erzeugt. Der Decoder puffert jedoch weniger Stichproben in diesem Modus, was möglicherweise zu Störungen führen kann, da der Decoder nicht so viele Frames im Voraus decodiert. Um den Modus mit geringer Latenz zu aktivieren, legen Sie das [ATTRIBUT CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) fest.
-   **Suchen.** Rufen Sie zur präzisen Suche die [**METHODE DERTRANSFORM::SetOutputBounds auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) Wenn diese Methode aufgerufen wird, gibt der Decoder nur Frames aus, die innerhalb des vom Aufrufer angegebenen Zeitstempelbereichs liegen.
-   **Miniaturansichtsgenerierungsmodus**. Dieser Modus ist für die schnelle Generierung von Miniaturbildern vorgesehen. In diesem Modus decodiert der Decoder anfänglich nur I-Frames. Wenn innerhalb einer bestimmten Anzahl von Frames kein I-Frame gefunden wird, beginnt der Decoder mit der Decodierung von P-Frames und gibt Nicht-I-Frames in einem festen Intervall aus (eins pro *N* Bilder), bis ein I-Frame erreicht ist. Um den Miniaturansichtsgenerierungsmodus zu aktivieren, legen Sie die [CODECAPI \_ AVDecVideoThumbnailGenerationMode-Eigenschaft](../directshow/avdecvideothumbnailgenerationmode-property.md) fest.
-   **Trickplay.** Der Decoder kann mit Raten schneller als in Echtzeit decodiert werden. Bei höheren Wiedergaberaten wechselt der Decoder zur Decodierung nur von I-Frames. Für die umgekehrte Wiedergabe werden nur I-Frames decodiert.

### <a name="codec-properties"></a>Codeceigenschaften

Der Decoder unterstützt die folgenden Eigenschaften über die [**ÜBERTRANSFORM::GetAttributes-Methode.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| Eigenschaft                                                                                                      | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Aktiviert oder deaktiviert den Miniaturansichtsgenerierungsmodus.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Aktiviert oder deaktiviert die hardwarebeschleunigte Decodierung.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Aktiviert oder deaktiviert den Modus mit niedriger Latenz.                                                                      |
| [\_MFT-DECODER \_ MACHT \_ \_ AUSGABETYPEN \_ IN \_ NATIVER REIHENFOLGE \_ VERFÜGBAR](mft-decoder-expose-output-types-in-native-order.md) | Gibt an, ob der Decoder Ausgabetypen verfügbar macht, die für die Transcodierung vor anderen Formaten geeignet sind. |



 

Von diesen Eigenschaften kann Folgendes auch über die [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) festgelegt werden:

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Einschränkungen

-   Der Decoder wird auf IA-64-basierten Plattformen nicht unterstützt.
-   Der Decoder unterstützt keine CSS-Entschlüsselung oder -Wiedergabe verschlüsselter DVDs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
