---
description: Gibt benutzerdefinierte Farb-Primärwerte für einen Video Medientyp an.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: MF_MT_CUSTOM_VIDEO_PRIMARIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349689"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_ \_ Benutzerdefiniertes MF MT- \_ \_ Attribut

Gibt benutzerdefinierte Farb-Primärwerte für einen Video Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

Bytearray

## <a name="remarks"></a>Bemerkungen

Bei den Attributdaten handelt es sich um eine [**\_ benutzerdefinierte MT- \_ Video \_ primär**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) Struktur

Dieses Attribut gibt die tatsächliche Farb Menge des Inhalts oder einer Anzeige an. CEA-861,3/SMPTE St. 2086 Color Volume-Debuginformationen werden von Decodern in diesem Attribut gespeichert. Beachten Sie, dass dieses Attribut das [**MF \_ MT- \_ Video- \_ Primary**](mf-mt-video-primaries-attribute.md)-Attribut nicht ersetzt. Dieses Attribut beschreibt einen Hinweis zum Farbvolumen des Inhalts, während die **MF- \_ MT-Video- \_ \_ primär** Punkte die Farb Replikate beschreiben, in denen der Inhalt tatsächlich codiert ist (z. b. die Bedeutung von 1,0 in den R/g/B-Kanälen einer Gleit Komma Darstellung).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




