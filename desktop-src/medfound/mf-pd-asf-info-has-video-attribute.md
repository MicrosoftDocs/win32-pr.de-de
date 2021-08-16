---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) mindestens einen Videostream enthält.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: MF_PD_ASF_INFO_HAS_VIDEO-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b5012a7fc20628cf8b50a4fc72242c02779623beb8126525a51501f51e412a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876271"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a>MF \_ PD \_ ASF INFO HAS \_ \_ \_ VIDEO-Attribut

Gibt an, ob eine ASF-Datei (Advanced Systems Format) mindestens einen Videostream enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalt. Wenn der Wert **TRUE** ist, verfügt die Datei über mindestens einen Videostream. Andernfalls enthält die Datei keine Videostreams.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




