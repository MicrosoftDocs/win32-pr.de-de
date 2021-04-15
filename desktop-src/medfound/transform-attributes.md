---
description: Transformations Attribute
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Transformations Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485339"
---
# <a name="transform-attributes"></a>Transformations Attribute

Die folgenden Attribute gelten entweder für [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs), für [Aktivierungs Objekte](activation-objects.md) für MFTs oder für beides.



| Attribut                                                                                                     | BESCHREIBUNG                                                                                                                                                                                   | Gilt für                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ Aktivierung von \_ MFT \_ gesperrt**](mf-activate-mft-locked-attribute.md)                                         | Gibt an, ob das topologielader die Medientypen in einer MFT ändert.                                                                                                                  | MFTs                        |
| [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md)                                                       | Gibt an, ob eine Media Foundation Transformation (MFT) eine DirectX-Video Beschleunigung unterstützt.                                                                                                     | MFTs                        |
| [MF- \_ Transformation \_ Async](mf-transform-async.md)                                                                | Gibt an, ob eine MFT die asynchrone Verarbeitung ausführt.                                                                                                                                    | MFTs                        |
| [MF- \_ Transformation \_ Async \_ Unlock](mf-transform-async-unlock.md)                                                 | Aktiviert die Verwendung eines asynchronen MFT.                                                                                                                                                       | MFTs                        |
| [Kategorie-Attribut der MF- \_ Transformation \_ \_](mf-transform-category-attribute.md)                                     | Gibt die Kategorie für einen MFT an.                                                                                                                                                            | MFT-Aktivierungs Objekte      |
| [MF \_ - \_ Transformationsflags- \_ Attribut](mf-transform-flags-attribute.md)                                           | Enthält Flags für ein MFT-Aktivierungs Objekt.                                                                                                                                                  | MFT-Aktivierungs Objekte      |
| [MFT- \_ Codec- \_ Verdienst \_ Attribut](mft-codec-merit-attribute.md)                                                 | Enthält den Wert eines Hardware Codecs.                                                                                                                                                 | MFT-Aktivierungs Objekte      |
| [MFT- \_ Attribut für verbundenen Daten \_ Strom \_](mft-connected-stream-attribute.md)                                       | Enthält einen Zeiger auf die streamattribute des verbundenen Streams auf einem hardwarebasierten MFT.                                                                                                  | MFTs                        |
| [mit \_ \_ dem HW- \_ \_ Stream verbundene MFT](mft-connected-to-hw-stream.md)                                              | Gibt an, ob ein Hardware basiertes MFT mit einem anderen hardwarebasierten MFT verbunden ist.                                                                                                            | MFTs                        |
| [MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen \_ in \_ nativer \_ Reihenfolge verfügbar.](mft-decoder-expose-output-types-in-native-order.md) | Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.                                                                                   | MFTs                        |
| [\_ \_ abschließende \_ Video \_ Auflösungs \_ Hinweis des MFT-Decoders](mft-decoder-final-video-resolution-hint.md)                   | Gibt die endgültige Ausgabeauflösung des decodierten Bilds nach der Videoverarbeitung an.                                                                                                           | MFTs                        |
| [MFT- \_ Encoder \_ unterstützt \_ config- \_ Ereignis](mft-encoder-supports-config-event.md)                                | Gibt an, dass der MFT-Encoder beim Streaming das Empfangen von [meencodingparameter](meencodingparameters.md) -Ereignissen unterstützt.                                                                     | MFTs                        |
| [LUID des MFT-Aufzählungs \_ \_ Adapters \_](mft-enum-adapter-luid.md)                                                         | Gibt einen eindeutigen Bezeichner für eine Grafikkarte an. Verwenden Sie dieses Attribut, wenn Sie MFTEnum2 aufrufen, um MFTs aufzulisten, die einem bestimmten Adapter zugeordnet sind.                                             | MFTs                        |
| [MFT-Aufzählungs \_ \_ Hardware-URL- \_ \_ Attribut](mft-enum-hardware-url-attribute.md)                                    | Enthält den symbolischen Link für ein Hardware basiertes MFT.                                                                                                                                          | MFTs/MFT-Aktivierungs Objekte |
| [ID-Attribut des MFT-Aufzählungs \_ \_ Hardware \_ Herstellers \_ \_](mft-enum-hardware-vendor-id-attribute.md)                       | Gibt die Hersteller-ID für eine hardwarebasierte Media Foundation Transformation an.                                                                                                                       | MFTs                        |
| [MFT-Aufzählungs \_ \_ \_ Attribut nur transcode \_](mft-enum-transcode-only-attribute.md)                                | Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.                                                                                                            | MFTs                        |
| [MFT \_ fieldofuse \_ Unlock- \_ Attribut](mft-fieldofuse-unlock-attribute.md)                                     | Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der zum Entsperren des MFT verwendet werden kann.                                                                            | MFT-Aktivierungs Objekte      |
| [MFT-Attribut "Anzeige \_ \_ Name" \_](mft-friendly-name-attribute.md)                                             | Enthält den anzeigen Amen für ein Hardware basiertes MFT.                                                                                                                                           | MFT-Aktivierungs Objekte      |
| [Attribute der MFT- \_ Eingabe \_ Typen \_](mft-input-types-attributes.md)                                               | Enthält die registrierten Eingabetypen für einen MFT.                                                                                                                                               | MFT-Aktivierungs Objekte      |
| [Attribute der MFT- \_ Ausgabe \_ Typen \_](mft-output-types-attributes.md)                                             | Enthält die registrierten Ausgabetypen für einen MFT.                                                                                                                                              | MFT-Aktivierungs Objekte      |
| [MFT- \_ bevorzugtes \_ Encoder- \_ Profil](mft-preferred-encoder-profile.md)                                         | Enthält Konfigurations Eigenschaften für einen Encoder.                                                                                                                                             | MFT-Aktivierungs Objekte      |
| [Bevorzugtes MFT- \_ \_ OutputType- \_ Attribut](mft-preferred-outputtype-attribute.md)                               | Gibt das bevorzugte Ausgabeformat für einen Encoder an.                                                                                                                                         | MFT-Aktivierungs Objekte      |
| [Bevorzugtes MFT- \_ \_ OutputType- \_ Attribut](mft-preferred-outputtype-attribute.md)                               | Gibt das bevorzugte Ausgabeformat für einen Encoder an.                                                                                                                                         | MFT-Aktivierungs Objekte      |
| [Lokales MFT- \_ Prozess \_ \_ Attribut](mft-process-local-attribute.md)                                             | Gibt an, ob ein MFT nur im Prozess der Anwendung registriert ist.                                                                                                                     | MFT-Aktivierungs Objekte      |
| [MFT \_ REMUX \_ Mark \_ I \_ Bild \_ als \_ Clean \_ Point](mft-remux-mark-i-picture-as-clean-point.md)                 | Gibt an, ob die e. 264-Video-REMUX-MFT I-Bilder als Clean Point markieren soll, um eine bessere Suchfunktion zu erzielen. Dadurch haben Sie die Möglichkeit, für Suchvorgänge in nicht konformen abschließenden MP4-Dateien Beschädigungen zu beschädigen. | MFT-Aktivierungs Objekte      |
| [MFT \_ -Unterstützung \_ 3dvideo](mft-support-3dvideo.md)                                                              | Gibt an, ob eine Media Foundation Transformation (MFT) 3D-stereografievideo unterstützt.                                                                                                          | MFT-Aktivierungs Objekte      |
| [**MFT- \_ Unterstützung für \_ dynamisches \_ Format \_ ändern**](mft-support-dynamic-format-change-attribute.md)                  | Gibt an, ob eine Media Foundation Transformation (MFT) dynamische Formatänderungen unterstützt.                                                                                                         | MFTs                        |
| [\_ \_ CLSID- \_ Attribut der MFT-Transformation](mft-transform-clsid-attribute.md)                                         | Enthält den Klassen Bezeichner (CLSID) einer MFT.                                                                                                                                              | MFT-Aktivierungs Objekte      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



