---
description: Enthält zusätzliche Formatdaten für einen Medientyp.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0196e8fea06bb84fe5a78a8b486f95864e0c6d889692dfa6f3ee9b1103da518a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012781"
---
# <a name="mf_mt_user_data-attribute"></a>MF \_ MT \_ USER \_ DATA-Attribut

Enthält zusätzliche Formatdaten für einen Medientyp.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Die Bedeutung der Daten in diesem Attribut hängt vom Format ab, das vom Medientyp beschrieben wird.



| Formattyp                                                                                                           | Zusätzliche Formatdaten                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Mediencodec.                                                                                                  | Codec private Daten.                                                                                                                       |
| Konvertierte [**VIDEOINFOHEADER-**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) oder [**VIDEOINFOHEADER2-Struktur.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)   | Zusätzliche Daten, die nach der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) angezeigt werden, ohne die Farbtabelle oder Farbmasken. |
| Konvertierte [**WAVEFORMATEX-**](/previous-versions/dd757713(v=vs.85)) oder [**WAVEFORMATEXTENSIBLE-Struktur.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) | Zusätzliche Daten, die nach der Audioformatstruktur angezeigt werden.                                                                                 |



 

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

[**ATTRIBUTEs::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEs::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
