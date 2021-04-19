---
description: Wird von einer Pipeline Komponente ausgelöst, wenn die Ausgabe Richtlinie für den Stream geändert wird. Dieses Ereignis gilt nur für geschützte Inhalte.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Mepolicychanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350556"
---
# <a name="mepolicychanged-event"></a>Mepolicychanged-Ereignis

Wird von einer Pipeline Komponente ausgelöst, wenn die Ausgabe Richtlinie für den Stream geändert wird. Dieses Ereignis gilt nur für geschützte Inhalte.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfoutputpolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) -Schnittstelle der neuen Richtlinie für den Datenstrom.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Alle vertrauenswürdigen Ausgaben müssen dieses Ereignis behandeln. Media Foundation Transformationen (MFTs) empfangen dieses Ereignis über die [**IMF Transform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) -Methode. Medien senken empfangen dieses Ereignis über die [**IMF streamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode.

Die vertrauenswürdige Ausgabe muss die neue Richtlinie anwenden oder die Fehlercode-MF- \_ E- \_ Richtlinie \_ nicht unterstützt zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




