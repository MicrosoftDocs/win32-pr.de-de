---
description: Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt dieses Attribut an, ob die Quelle auch eine Verdünnung anfordert. Eine Definition der Verdünnung finden Sie unter Informationen zur Raten Kontrolle.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959048"
---
# <a name="mf_event_do_thinning-attribute"></a>MF-Ereignis, das das \_ \_ Attribut durch \_ dünden

Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt dieses Attribut an, ob die Quelle auch eine Verdünnung anfordert. Eine Definition der Verdünnung finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [mesourceratechangerequused](mesourceratechangerequested.md) -Ereignis verwendet. Wenn der Wert **true** ist, fordert die Medienquelle einen Switch zur dünnen Wiedergabe an.

Der Standardwert ist **FALSE**.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




