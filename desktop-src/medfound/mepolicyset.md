---
description: 'Wird von einer Output Trust Authority (OTA) ausgelöst, wenn die IMF outputtrustauthority:: setpolicy-Methode asynchron abgeschlossen wird.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: MEPolicySet-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356605"
---
# <a name="mepolicyset-event"></a>MEPolicySet-Ereignis

Wird von einer Output Trust Authority (OTA) ausgelöst, wenn die [**IMF outputtrustauthority:: setpolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) -Methode asynchron abgeschlossen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |
| VT \_ UI4<br/> | Ein Bezeichner, der für eine [IMF outputpolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) über das [MF_POLICY_ID](mf-policy-id.md) -Attribut festgelegt werden kann.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




