---
description: Wird von einer streamsenke ausgelöst, wenn sich die Rate geändert hat.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Mestreamsinkratechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349359"
---
# <a name="mestreamsinkratechanged-event"></a>Mestreamsinkratechanged-Ereignis

Wird von einer streamsenke ausgelöst, wenn sich die Rate geändert hat.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn eine streamsenke Raten Änderungen unterstützt, sendet Sie dieses Ereignis, nachdem die Raten Änderung durchgeführt wurde. Das Ereignis wird einmal für jeden Aufrufe der [**imfclockstaatink:: onclockertrate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode der Senke gesendet. Wenn die Raten Änderung nicht erfolgreich ist, ist der Ereignis Statuswert ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> </dl>

 

 




