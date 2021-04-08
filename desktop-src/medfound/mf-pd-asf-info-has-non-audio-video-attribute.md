---
description: Gibt an, ob die Datei "Advanced Systems Format (ASF)" Streams enthält, die keine Audiodaten oder Videos enthalten.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960191"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a>MF \_ PD \_ \_ -ASF \_ -Info hat \_ nicht \_ \_ Audiovideo-Attribut

Gibt an, ob die Datei "Advanced Systems Format (ASF)" Streams enthält, die keine Audiodaten oder Videos enthalten.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt. Wenn der Wert **true** ist, enthält die Datei mindestens einen Datenstrom, der weder Audiodaten noch Video enthält. Beispiele hierfür sind Bild Datenströme, Skript Befehle und benutzerdefinierte beliebige Daten.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> </dl>

 

 




