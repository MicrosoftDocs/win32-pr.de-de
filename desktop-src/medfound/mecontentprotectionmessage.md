---
description: Wird von einer Pipeline Komponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabe Schutz Schemas ändert. Dieses Ereignis gilt nur für geschützte Inhalte.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Mecontentschutzmessage-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753184"
---
# <a name="mecontentprotectionmessage-event"></a>Mecontentschutzmessage-Ereignis

Wird von einer Pipeline Komponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabe Schutz Schemas ändert. Dieses Ereignis gilt nur für geschützte Inhalte.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Alle vertrauenswürdigen Ausgaben müssen dieses Ereignis behandeln. Media Foundation Transformationen (MFTs) empfangen dieses Ereignis über die [**IMF Transform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) -Methode. Medien senken empfangen dieses Ereignis über die [**IMF streamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode.

Die vertrauenswürdige Ausgabe muss die Richtlinien Änderungen anwenden oder die Fehlercode-MF- \_ E- \_ Richtlinie \_ nicht unterstützt zurückgeben.

Die Ereignisdaten und Attribute sind vom verwendeten Inhalts Schutzsystem abhängig.

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

 

 




