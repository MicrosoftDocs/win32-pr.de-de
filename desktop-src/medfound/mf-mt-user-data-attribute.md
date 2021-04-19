---
description: Enthält zusätzliche Formatierungsdaten für einen Medientyp.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351011"
---
# <a name="mf_mt_user_data-attribute"></a>\_ \_ Benutzer \_ Daten Attribut für MF-MT

Enthält zusätzliche Formatierungsdaten für einen Medientyp.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Die Bedeutung der Daten in diesem Attribut hängt von dem Format ab, das vom Medientyp beschrieben wird.



| Formattyp                                                                                                           | Zusätzliche Formatierungsdaten                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media-Codec.                                                                                                  | Private Codec-Daten.                                                                                                                       |
| Die konvertierte [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur.   | Zusätzliche Daten, die nach der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur angezeigt werden, ohne die Farbtabelle oder Farb Masken. |
| Konvertierte [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -oder [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur. | Zusätzliche Daten, die nach der audioformatstruktur angezeigt werden.                                                                                 |



 

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

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
