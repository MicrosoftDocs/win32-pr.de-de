---
description: Enthält die Startzeit, bei der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393557"
---
# <a name="mf_event_source_actual_start-attribute"></a>Das \_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle

Enthält die Startzeit, bei der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [mesourcestarted](mesourcestarted.md) -Ereignis verwendet. Das-Attribut ist relevant, wenn die Ereignisdaten leer sind (**VT \_ empty**), was darauf hinweist, dass die Medienquelle von der aktuellen Wiedergabe Position gestartet wurde. In diesem Fall gibt das **\_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle** die tatsächliche Startzeit an. Wenn die Ereignisdaten **VT \_ empty** sind und dieses Attribut nicht festgelegt ist, wird für die Startzeit der Wert 0 (null) angenommen.

Wenn die [mesourcestarted](mesourcestarted.md) -Ereignisdaten die Startzeit (**VT \_ I8**) enthalten, sollte dieses Attribut nicht festgelegt werden.

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.

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

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




