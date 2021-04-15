---
description: Enthält einen Medientyp, der in einem anderen Medientyp umschließt wurde.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: MF_MT_WRAPPED_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393258"
---
# <a name="mf_mt_wrapped_type-attribute"></a>In das MF- \_ \_ Attribut umschließtes \_

Enthält einen Medientyp, der in einem anderen Medientyp umschließt wurde.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird in der [**MF wrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) -Funktion verwendet, die einen Medientyp in einem anderen Medientyp umschließt.

Die Funktion [**MF wrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) führt folgende Aktionen aus:

1.  Konvertiert den ursprünglichen Medientyp in ein binäres Array.
2.  Legt das vom MF-Attribut **\_ \_ umschließte \_ Type** -Attribut für den neuen Medientyp fest. Der Wert des-Attributs ist das binäre Array.

Anwendungen verwenden dieses Attribut in der Regel nicht direkt. Um den ursprünglichen Medientyp zu entpacken, nennen Sie [**mfunwrapmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).

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

 

 




