---
description: Wird von DER QUELLEMEDIASOURCE gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: MEVideoCaptureDeviceRemoved-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f209dc4be6e8f45639b060de1328cb04c932463f6b76355b7538b5649a69634e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013480"
---
# <a name="mevideocapturedeviceremoved-event"></a>MEVideoCaptureDeviceRemoved-Ereignis

Wird von [**DER QUELLEMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE               | Beschreibung                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von [**DERENMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




