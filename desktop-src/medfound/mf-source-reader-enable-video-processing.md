---
description: Ermöglicht die Videoverarbeitung durch den Quell Reader.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484806"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>MF- \_ Quell \_ Leser Aktivieren von \_ \_ Video \_ Verarbeitungs Attributen

Ermöglicht die Videoverarbeitung durch den [Quell Reader](source-reader.md).

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                                                                                                                | Bedeutung                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Ungleich NULL**</dt> </dl> | Aktivieren Sie die Videoverarbeitung.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Zins**</dt> </dl>             | Deaktivieren Sie die Videoverarbeitung. (Standardwert)<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** (ungleich 0 (null)) ist, kann der Quell Leser die folgende eingeschränkte Videoverarbeitung für nicht komprimierte Video Frames ausführen:

-   Konvertierung von YUV in RGB-32.
-   Deinterlacing.

Diese Vorgänge werden in Software ausgeführt und sind nicht für die Wiedergabe optimiert. Diese Funktion ist für Anwendungen vorgesehen, die eine kleine Anzahl von Frames verarbeiten, z. –. um eine Video Miniaturansicht zu erstellen – oder Anwendungen, die Frames nicht in Echtzeit decodieren. Der Deinterlacing-Vorgang interpoliert Daten aus einem einzelnen Feld und ist daher verlustfrei.

Vermeiden Sie diese Einstellung, wenn Sie Direct3D verwenden, um die Video Frames anzuzeigen, da die GPU in der Regel bessere Video Verarbeitungsfunktionen bereitstellt.

Wenn dieses Attribut " **true**" ist, müssen die folgenden Attribute " **false**" lauten:

-   [MF- \_ Quell \_ Leser \_ D3D \_ Manager](mf-source-reader-d3d-manager.md)
-   [MF- \_ Lese Schreibvorgänge \_ Deaktivieren \_](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




