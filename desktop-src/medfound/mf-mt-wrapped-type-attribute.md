---
description: Enthält einen Medientyp, der von einem anderen Medientyp umschlossen wurde.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: MF_MT_WRAPPED_TYPE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ec0b86f985e40f808862091d3ea4506d8c456ffbf05ebd749f15e8ba8bf0c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119356360"
---
# <a name="mf_mt_wrapped_type-attribute"></a>MF \_ MT \_ WRAPPED \_ TYPE-Attribut

Enthält einen Medientyp, der von einem anderen Medientyp umschlossen wurde.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut wird in der [**MFWrapMediaType-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) verwendet, die einen Medientyp in einem anderen Medientyp umschließt.

Die [**MFWrapMediaType-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) führt Folgendes aus:

1.  Konvertiert den ursprünglichen Medientyp in ein binäres Array.
2.  Legt das **MF \_ MT \_ WRAPPED \_ TYPE-Attribut** für den neuen Medientyp fest. Der Wert des Attributs ist das binäre Array.

Anwendungen verwenden dieses Attribut in der Regel nicht direkt. Um den ursprünglichen Medientyp zu entpacken, rufen Sie [**MFUnwrapMediaType auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




