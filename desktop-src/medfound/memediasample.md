---
description: 'Wird gesendet, wenn ein Mediendaten Strom ein neues Beispiel als Reaktion auf einen imfmediastream:: requestsample-Rückruf liefert.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Memediasample-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106369930"
---
# <a name="memediasample-event"></a>Memediasample-Ereignis

Wird gesendet, wenn ein Mediendaten Strom ein neues Beispiel als Reaktion auf einen [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)-Rückruf liefert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle des Beispiels.<br/> <br/> |



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

[Medienquellen](media-sources.md)
</dt> </dl>

 

 




