---
description: Wird von imfmediasource gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät vorzeitig entfernt wurde.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Mevideocapturedevicepreempted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348515"
---
# <a name="mevideocapturedevicepreempted-event"></a>Mevideocapturedevicepreempted-Ereignis

Wird von [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät vorzeitig entfernt wurde.

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

 

 




