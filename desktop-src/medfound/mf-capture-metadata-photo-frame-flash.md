---
description: Gibt an, ob ein Flash für den erfassten Frame ausgelöst wurde.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a885786674c524b382912100171502dba78a010b2169738233b5aaad88ed701a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973919"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>MF \_ CAPTURE METADATA PHOTO FRAME \_ \_ \_ \_ FLASH-Attribut

Gibt an, ob ein Flash für den erfassten Frame ausgelöst wurde.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                               | Bedeutung                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | In diesem Frame wurde kein Flash ausgelöst.<br/>                                                                                                   |
| <dl> <dt>ungleich null</dt> </dl> | Für diesen Frame wurde ein Flash ausgelöst.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reserviert<br/> Überprüfen Sie nicht explizit auf den Wert 1. Anwendungen sollten nur auf !=0 überprüfen, um anzugeben, ob ein Flash ausgelöst wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




