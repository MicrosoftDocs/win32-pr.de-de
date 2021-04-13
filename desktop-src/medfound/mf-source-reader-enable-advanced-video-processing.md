---
description: Ermöglicht die erweiterte Videoverarbeitung durch den Quell Leser, einschließlich der Farb Raum Konvertierung, der Deinterlacing, der Videogröße und der Konvertierung von Frameraten.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525997"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>MF- \_ Quell \_ Leser Aktivieren des \_ \_ erweiterten \_ Video \_ Verarbeitungs Attributs

Ermöglicht die erweiterte Videoverarbeitung durch den [Quell Leser](source-reader.md), einschließlich der Farb Raum Konvertierung, der Deinterlacing, der Videogröße und der Konvertierung von Frameraten.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** ist, kann der Quell Leser einen Videoprozessor in die Verarbeitungs Pipeline einfügen, wodurch die folgenden Typen von Formatkonvertierungen aktiviert werden:

-   Farb Raum Konvertierung (YUV in RGB-32)
-   Deinterlacing
-   Ändern der Größe von Videos
-   Umwandlung von Frame Raten

Wenn dieses Attribut **true** ist, muss das MF-Attribut "read [ \_ Write \_ deaktivierte \_ Konverter](mf-readwrite-disable-converters.md) " den Wert **false** aufweisen.

Der Quell Leser sucht nach Video Prozessoren, die in der Kategorie **\_ \_ Video \_ Prozessor Kategorie der Kategorie MFT** registriert sind, einschließlich der für den lokalen Prozess registrierten MFTs. (Weitere Informationen zur lokalen Registrierung von MFTs finden Sie unter [**MF tregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) .) Der Quell Leser verwendet den Transcode-Videoprozessor (xvp), wenn kein anderer geeigneter Videoprozessor gefunden wurde.

Die Anwendung gibt den gewünschten Ausgabetyp an, indem [**imfsourcereader:: setcurrentmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)aufgerufen wird. Wenn der Quell Leser den Videoprozessor konfiguriert, versucht er, die folgenden Attribute des Ausgabe Typs abzugleichen:

-   Frame Rate ([MF- \_ MT-Frame- \_ \_ Rate](mf-mt-frame-rate-attribute.md))
-   Frame Größe ([MF- \_ MT- \_ Rahmen \_ Größe](mf-mt-frame-size-attribute.md))
-   Interlace-Modus ([MF- \_ MT- \_ Interlace- \_ Modus](mf-mt-interlace-mode-attribute.md))
-   Pixel Seitenverhältnis ([MF- \_ MT-Pixel- \_ \_ Seiten \_ Verhältnis](mf-mt-pixel-aspect-ratio-attribute.md))
-   Untertyp ([MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md))

Dieses Attribut ähnelt dem MF- [ \_ Quell \_ Lesegerät zum \_ Aktivieren von \_ Video \_ Verarbeitungs](mf-source-reader-enable-video-processing.md) Attributen, bietet jedoch die folgenden Vorteile:

-   Es wird ein größerer Bereich von Formatkonvertierungen unterstützt.
-   Anwendungen können Ihre eigenen Konverter registrieren.
-   Einige Konvertierungen können in Hardware mithilfe der GPU ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




