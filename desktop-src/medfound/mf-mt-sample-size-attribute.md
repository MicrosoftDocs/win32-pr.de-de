---
description: Gibt die Größe der einzelnen Stichproben in Bytes in einem Medientyp an.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: MF_MT_SAMPLE_SIZE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368199"
---
# <a name="mf_mt_sample_size-attribute"></a>Attribut der MF \_ MT- \_ Stichproben \_ Größe

Gibt die Größe der einzelnen Stichproben in Bytes in einem Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur gültig, wenn das MF MT-Attribut " [**\_ \_ Fixed \_ size \_ Samples**](mf-mt-fixed-size-samples-attribute.md) " den Wert **true** hat.

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

 

 




