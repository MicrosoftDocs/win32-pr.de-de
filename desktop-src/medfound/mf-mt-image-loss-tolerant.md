---
description: Gibt an, ob ein ASF-Bildstream ein abbaubarer JPEG-Typ ist.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862747"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>Das MF \_ MT- \_ Image \_ Verlust \_ tolerantes Attribut

Gibt an, ob ein ASF-Bildstream ein abbaubarer JPEG-Typ ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für den Medientyp für bildstreams in ASF. Wenn der Wert **true** ist, ist der Datenstrom ein abbaubarer JPEG-Bildtyp. Andernfalls ist der Stream ein jff-Bildtyp. Weitere Informationen zu diesen Streamtypen finden Sie in der ASF-Spezifikation.

Zusätzlich zum Attribut "MF \_ MT \_ Image \_ Loss \_ tolerante" enthält der Medientyp für einen ASF-Bildstream die folgenden Attribute:



| Attribut                                                 | BESCHREIBUNG                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | Enthält den Wert des **MF MediaType- \_ Bilds**. |
| [**MF- \_ MT- \_ Frame \_ Größe**](mf-mt-frame-size-attribute.md) | Gibt die Bildgröße in Pixel an.            |



 

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




