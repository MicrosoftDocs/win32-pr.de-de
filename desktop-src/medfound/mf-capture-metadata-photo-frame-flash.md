---
description: Gibt an, ob ein Flash für den aufgezeichneten Frame ausgelöst wurde.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349105"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>"MF \_ Capture \_ Metadata \_ Photo \_ Frame \_ Flash Attribute"

Gibt an, ob ein Flash für den aufgezeichneten Frame ausgelöst wurde.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                               | Bedeutung                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | Ein Flash wurde für diesen Frame nicht ausgelöst.<br/>                                                                                                   |
| <dl> <dt>ungleich null</dt> </dl> | Ein Flash wurde für diesen Frame ausgelöst.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reserviert<br/> Überprüfen Sie nicht explizit den Wert 1. Anwendungen sollten nur nach! = 0 suchen, um anzugeben, ob ein Flash ausgelöst wurde.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




