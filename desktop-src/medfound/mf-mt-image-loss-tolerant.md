---
description: Gibt an, ob ein ASF-Bildstream ein heruntersetzbarer JPEG-Typ ist.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdf5b2633586cf4b73279a636119ac4770a5321d6bc22b5b961fa85881019b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035168"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>MF \_ MT IMAGE LOSS \_ \_ \_ TOLERANT-Attribut

Gibt an, ob ein ASF-Bildstream ein heruntersetzbarer JPEG-Typ ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für den Medientyp für Bildstreams in ASF. Wenn der Wert **TRUE ist,** ist der Stream ein heruntersetzbarer JPEG-Bildtyp. Andernfalls ist der Stream ein JFIF-Imagetyp. Weitere Informationen zu diesen Streamtypen finden Sie in der ASF-Spezifikation.

Zusätzlich zum MF MT IMAGE LOSS TOLERANT-Attribut enthält der Medientyp für einen \_ \_ \_ \_ ASF-Imagestream die folgenden Attribute:



| attribute                                                 | Beschreibung                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md) | Enthält den Wert **MFMediaType \_ Image**. |
| [**MF \_ MT \_ FRAME \_ SIZE**](mf-mt-frame-size-attribute.md) | Gibt die Bildgröße in Pixel an.            |



 

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




