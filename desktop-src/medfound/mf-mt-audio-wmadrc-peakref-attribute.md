---
description: Verweis Spitzen Volume-Ebene einer Windows Media Audio Datei.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: MF_MT_AUDIO_WMADRC_PEAKREF-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528241"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a>MF \_ MT \_ -Audiodatei \_ wmadrc- \_ Attribut (Peer)

Verweis Spitzen Volume-Ebene einer Windows Media Audio Datei.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für audiomedientypen für Windows Media Audio Codecs. Gibt die ursprüngliche maximale Volumeebene für den Inhalt an. Der Decoder kann diesen Wert verwenden, um ein dynamisches Bereichs Steuerelement auszuführen.

Die [**imfasfcontentinfo::P archeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/wmadrcpeer Reference-**](../wmformat/wm-wmadrcpeakreference.md) Attribut enthält. Dieses Attribut ist in der Dokumentation zum Windows Media-Format SDK dokumentiert.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
