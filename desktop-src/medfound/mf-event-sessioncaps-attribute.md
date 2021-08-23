---
description: Enthält Flags, die die Funktionen der Mediensitzung basierend auf der aktuellen Präsentation definieren.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: MF_EVENT_SESSIONCAPS -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175c81d1cc231204060a63a90ffe9e2432b73bdec35c7885dea203416995ea92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973789"
---
# <a name="mf_event_sessioncaps-attribute"></a>MF \_ EVENT \_ SESSIONCAPS-Attribut

Enthält Flags, die die Funktionen der Mediensitzung basierend auf der aktuellen Präsentation definieren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut enthält ein bitweises **OR** von null oder mehr Flags. Eine Liste der möglichen Flags finden Sie unter 1000000000000000000000000000000000000000000000000 [](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities)

Dieses Attribut wird mit dem [MESessionCapabilitiesChanged-Ereignis](mesessioncapabilitieschanged.md) verwendet.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




