---
description: Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: MF_EVENT_SESSIONCAPS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347879"
---
# <a name="mf_event_sessioncaps-attribute"></a>MF- \_ Ereignis \_ sessioncaps-Attribut

Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut enthält ein bitweises **or** von 0 (null) oder mehr Flags. Eine Liste möglicher Flags finden Sie unter [**imfmediasession:: gezession-Funktionen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).

Dieses Attribut wird mit dem [mesessioncapabilitieschge](mesessioncapabilitieschanged.md) -Ereignis verwendet.

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

 

 




