---
description: Referenz zur durchschnittlichen Volumeebene einer Windows Medienaudiodatei.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: MF_MT_AUDIO_WMADRC_AVGREF -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a822046d368025bcfd068f7c1afd32f75d22b5d1ceab69d3e4b517595baa9b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035288"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a>MF \_ MT \_ AUDIO \_ WMADRC \_ AVGREF-Attribut

Referenz zur durchschnittlichen Volumeebene einer Windows Medienaudiodatei.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Audiomedientypen für Windows Medienaudiocodecs. Sie gibt die ursprüngliche durchschnittliche Volumeebene des Inhalts an. Der Decoder kann diesen Wert verwenden, um eine dynamische Bereichssteuerung durchzuführen.

Die [**IMFASFContentInfo::P arseHeader-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/WMADRCAverageReference-Attribut**](../wmformat/wm-wmadrcaveragereference.md) enthält. Dieses Attribut ist in der Dokumentation zum Windows Media Format SDK dokumentiert.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
