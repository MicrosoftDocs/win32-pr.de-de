---
description: Durchschnittliche Zielvolumeebene einer Windows Medienaudiodatei.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: MF_MT_AUDIO_WMADRC_AVGTARGET Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a05ef07966313d9b06bec57ec09af068f385bbc869cba7fab33e42e786dc63b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940630"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>MF \_ MT \_ AUDIO \_ WMADRC \_ AVGTARGET-Attribut

Durchschnittliche Zielvolumeebene einer Windows Medienaudiodatei.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Audiomedientypen für Windows Medienaudiocodecs. Sie gibt die durchschnittliche Zielvolumeebene des Inhalts an. Der Decoder kann diesen Wert verwenden, um die Steuerung des dynamischen Bereichs auszuführen.

Die [**IMFASFContentInfo::P arseHeader-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/WMADRCAverageTarget-Attribut**](../wmformat/wm-wmadrcaveragetarget.md) enthält. Dieses Attribut ist in der Dokumentation Windows Media Format SDK dokumentiert.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
