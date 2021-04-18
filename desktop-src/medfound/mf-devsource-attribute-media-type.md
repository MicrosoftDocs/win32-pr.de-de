---
description: Gibt das Ausgabeformat eines Geräts an.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354909"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>Attribut für \_ \_ \_ \_ Medientyp des MF-devsource-Attributs

Gibt das Ausgabeformat eines Geräts an.

## <a name="data-type"></a>Datentyp

**[**MFT \_ Registrieren \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** von als **\[ Byte \]** gespeicherten Typinformationen

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut enthält ein paar von GUIDs: einen Haupttyp und einen Untertyp. Diese GUIDs beschreiben das Standardausgabeformat des Geräts. Das Gerät unterstützt möglicherweise zusätzliche Ausgabeformate.

Wenn z. b. ein Video Erfassungsgerät das RGB-32-Video ausgibt, ist der Wert dieses Attributs `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Dieses Attribut ist ein Hinweis für die Anwendung. Um das genaue Ausgabeformat zu erhalten, erstellen Sie die Medienquelle für das Gerät, und rufen Sie den Präsentations Deskriptor der Medienquelle ab.

Dieses Attribut wird für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 




