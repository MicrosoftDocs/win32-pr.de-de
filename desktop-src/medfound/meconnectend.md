---
description: Wird von der Netzwerkquelle ausgelöst, wenn das Öffnen einer URL abgeschlossen ist.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Meconnectend-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355531"
---
# <a name="meconnectend-event"></a>Meconnectend-Ereignis

Wird von der Netzwerkquelle ausgelöst, wenn das Öffnen einer URL abgeschlossen ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Netzwerkquelle sendet dieses Ereignis direkt über die [**imfsourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode der Anwendung an die Anwendung, nicht über die übliche [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF sourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




