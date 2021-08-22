---
description: Transformieren von Attributen
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Transformieren von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d5b7a5f4ff6174a48058c81fe1cdea382b18c058985da803efa4110eb12e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034561"
---
# <a name="transform-attributes"></a>Transformieren von Attributen

Die folgenden Attribute gelten entweder für Media Foundation [Transformationen](media-foundation-transforms.md) (MFTs) oder für [Aktivierungsobjekte](activation-objects.md) für MFTs oder beides.



| attribute                                                                                                     | Beschreibung                                                                                                                                                                                   | Gilt für                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ ACTIVATE \_ MFT \_ LOCKED**](mf-activate-mft-locked-attribute.md)                                         | Gibt an, ob das Topologielader die Medientypen auf einem MFT ändert.                                                                                                                  | Mfts                        |
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                                                       | Gibt an, ob eine Media Foundation Transformation (MFT) die DirectX-Videobeschleunigung unterstützt.                                                                                                     | Mfts                        |
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                                                | Gibt an, ob ein MFT eine asynchrone Verarbeitung ausführt.                                                                                                                                    | Mfts                        |
| [MF \_ TRANSFORM \_ ASYNC \_ UNLOCK](mf-transform-async-unlock.md)                                                 | Ermöglicht die Verwendung eines asynchronen MFT.                                                                                                                                                       | Mfts                        |
| [MF \_ TRANSFORM \_ \_ CATEGORY-Attribut](mf-transform-category-attribute.md)                                     | Gibt die Kategorie für eine MFT an.                                                                                                                                                            | MFT-Aktivierungsobjekte      |
| [MF \_ TRANSFORM \_ FLAGS-Attribut \_](mf-transform-flags-attribute.md)                                           | Enthält Flags für ein MFT-Aktivierungsobjekt.                                                                                                                                                  | MFT-Aktivierungsobjekte      |
| [MFT \_ \_ CODEC-ATTRIBUT \_ "CODIERT"](mft-codec-merit-attribute.md)                                                 | Enthält den Wert eines Hardwarecodecs.                                                                                                                                                 | MFT-Aktivierungsobjekte      |
| [MFT \_ CONNECTED \_ \_ STREAM-ATTRIBUT](mft-connected-stream-attribute.md)                                       | Enthält einen Zeiger auf die Streamattribute des verbundenen Streams auf einem hardwarebasierten MFT.                                                                                                  | Mfts                        |
| [MFT \_ MIT \_ \_ HW-STREAM \_ VERBUNDEN](mft-connected-to-hw-stream.md)                                              | Gibt an, ob ein hardwarebasiertes MFT mit einem anderen hardwarebasierten MFT verbunden ist.                                                                                                            | Mfts                        |
| [\_MFT-DECODER \_ MACHT \_ \_ AUSGABETYPEN \_ IN \_ NATIVER REIHENFOLGE \_ VERFÜGBAR](mft-decoder-expose-output-types-in-native-order.md) | Gibt an, ob ein Decoder IYUV/I420-Ausgabetypen (geeignet für die Transcodierung) vor anderen Formaten verfügbar macht.                                                                                   | Mfts                        |
| [HINWEIS ZUR \_ \_ ENDGÜLTIGEN \_ VIDEOAUFLÖSUNG DES \_ \_ MFT-DECODERS](mft-decoder-final-video-resolution-hint.md)                   | Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.                                                                                                           | Mfts                        |
| [MFT \_ ENCODER \_ UNTERSTÜTZT \_ \_ KONFIGURATIONSEREIGNIS](mft-encoder-supports-config-event.md)                                | Gibt an, dass der MFT-Encoder das Empfangen von [MEEncodingParameter-Ereignissen während](meencodingparameters.md) des Streamings unterstützt.                                                                     | Mfts                        |
| [\_ \_ MFT-ENUM-ADAPTER-LUID \_](mft-enum-adapter-luid.md)                                                         | Gibt einen eindeutigen Bezeichner für eine Grafikkarte an. Verwenden Sie dieses Attribut, wenn Sie MFTEnum2 aufrufen, um MFTs zu aufzählen, die einem bestimmten Adapter zugeordnet sind.                                             | Mfts                        |
| [\_ \_ \_ MFT-ENUM-HARDWARE-URL-Attribut \_](mft-enum-hardware-url-attribute.md)                                    | Enthält die symbolische Verknüpfung für ein hardwarebasiertes MFT.                                                                                                                                          | MFTs/MFT-Aktivierungsobjekte |
| [MFT \_ ENUM \_ HARDWARE \_ VENDOR \_ ID \_ Attribute](mft-enum-hardware-vendor-id-attribute.md)                       | Gibt die Anbieter-ID für eine hardwarebasierte Media Foundation An                                                                                                                       | Mfts                        |
| [\_ \_ MFT-ENUM-TRANSCODIERUNGSATTRIBUT \_ \_](mft-enum-transcode-only-attribute.md)                                | Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.                                                                                                            | Mfts                        |
| [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md)                                     | Enthält einen 50000001115555555555555555555555555555555555555555555555555555555555 [](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)                                                                            | MFT-Aktivierungsobjekte      |
| [MFT \_ FRIENDLY \_ \_ NAME-Attribut](mft-friendly-name-attribute.md)                                             | Enthält den Anzeigenamen für ein hardwarebasiertes MFT.                                                                                                                                           | MFT-Aktivierungsobjekte      |
| [MFT \_ INPUT \_ \_ TYPES-Attribute](mft-input-types-attributes.md)                                               | Enthält die registrierten Eingabetypen für eine MFT.                                                                                                                                               | MFT-Aktivierungsobjekte      |
| [Attribute für \_ \_ MFT-AUSGABETYPEN \_](mft-output-types-attributes.md)                                             | Enthält die registrierten Ausgabetypen für eine MFT.                                                                                                                                              | MFT-Aktivierungsobjekte      |
| [MFT \_ PREFERRED \_ ENCODER \_ PROFILE](mft-preferred-encoder-profile.md)                                         | Enthält Konfigurationseigenschaften für einen Encoder.                                                                                                                                             | MFT-Aktivierungsobjekte      |
| [MFT \_ PREFERRED \_ OUTPUTTYPE-Attribut \_](mft-preferred-outputtype-attribute.md)                               | Gibt das bevorzugte Ausgabeformat für einen Encoder an.                                                                                                                                         | MFT-Aktivierungsobjekte      |
| [MFT \_ PREFERRED \_ OUTPUTTYPE-Attribut \_](mft-preferred-outputtype-attribute.md)                               | Gibt das bevorzugte Ausgabeformat für einen Encoder an.                                                                                                                                         | MFT-Aktivierungsobjekte      |
| [MFT \_ PROCESS \_ \_ LOCAL-Attribut](mft-process-local-attribute.md)                                             | Gibt an, ob ein MFT nur im Prozess der Anwendung registriert ist.                                                                                                                     | MFT-Aktivierungsobjekte      |
| [MFT \_ REMUX \_ MARKIEREN SIE DAS BILD ALS \_ \_ \_ \_ \_ BEREINIGTEN PUNKT.](mft-remux-mark-i-picture-as-clean-point.md)                 | Gibt an, ob das H.264-Video remux MFT I-Bilder als bereinigten Punkt markieren soll, um eine bessere Suchfähigkeit zu erreichen. Dies kann zu Beschädigungen bei Suchern in nicht konformen endgültigen MP4-Dateien führen. | MFT-Aktivierungsobjekte      |
| [\_MFT-UNTERSTÜTZUNG \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Gibt an, ob Media Foundation-Transformation (MFT) 3D-Stereoaufzeichnungen unterstützt.                                                                                                          | MFT-Aktivierungsobjekte      |
| [**MFT-UNTERSTÜTZUNG \_ \_ FÜR DYNAMISCHE \_ \_ FORMATÄNDERUNG**](mft-support-dynamic-format-change-attribute.md)                  | Gibt an, ob eine Media Foundation Transform (MFT) dynamische Formatänderungen unterstützt.                                                                                                         | Mfts                        |
| [MFT \_ TRANSFORM \_ CLSID-Attribut \_](mft-transform-clsid-attribute.md)                                         | Enthält den Klassenbezeichner (CLSID) eines MFT.                                                                                                                                              | MFT-Aktivierungsobjekte      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



