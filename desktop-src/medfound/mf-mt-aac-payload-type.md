---
description: Gibt den Nutz Lasttyp eines AAC-Streams (Advanced audiocoding) an.
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: MF_MT_AAC_PAYLOAD_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358230"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>MF \_ MT- \_ AAC-Attribut für \_ Nutz Last \_ Typen

Gibt den Nutz Lasttyp eines AAC-Streams (Advanced audiocoding) an.

## <a name="data-type"></a>Datentyp

**UINT32**

Die folgenden Werte sind möglich.



| Wert                                                                        | Bedeutung                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Stream enthält \_ nur Rohdaten \_ Block Elemente.<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Der audiodatentransport-Stream (ADTs). Der Stream enthält eine \_ von MPEG-2 definierte ADTs-Sequenz.<br/>                       |
| <dl> <dt>2</dt> </dl> | Das Format für den audiodatenaustausch (ADIF). Der Stream enthält eine ADIF \_ -Sequenz, wie in MPEG-2 definiert.<br/>                     |
| <dl> <dt>3</dt> </dl> | Der Stream enthält einen MPEG-4-audiotransportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).<br/> |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Der MF \_ MT- \_ AAC- \_ Nutz \_ Lasttyp ist optional. Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream \_ \_ nur rohdatenblock-Elemente enthält.

Gilt nur für **mfaudioformat- \_ AAC**.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




