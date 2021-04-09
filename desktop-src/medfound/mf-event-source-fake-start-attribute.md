---
description: Gibt an, ob die aktuelle Segment Topologie leer ist.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: MF_EVENT_SOURCE_FAKE_START-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869119"
---
# <a name="mf_event_source_fake_start-attribute"></a>\_ \_ \_ Gefälschtes \_ Start Attribut der MF-Ereignis Quelle

Gibt an, ob die aktuelle Segment Topologie leer ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [mesourcestarted](mesourcestarted.md) -Ereignis verwendet.

Die Sequencer-Quelle legt dieses Attribut auf **true** fest, wenn die aktuelle Segment Topologie leer ist. Wenn dieses Attribut **true** ist, wurde die Wiedergabe noch nicht gestartet. Der Standardwert dieses Attributs ist **false**.

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

 

 




