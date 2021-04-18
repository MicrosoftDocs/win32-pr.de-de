---
description: Wird von imfmediasource gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Mevideocapturedeviceremoved-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357912"
---
# <a name="mevideocapturedeviceremoved-event"></a>Mevideocapturedeviceremoved-Ereignis

Wird von [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ leer <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von der [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




