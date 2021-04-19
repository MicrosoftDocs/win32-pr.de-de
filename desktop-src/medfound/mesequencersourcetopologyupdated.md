---
description: 'Wird von der Sequencer-Quelle ausgelöst, wenn die IMF sequencersource:: updatetopology-Methode asynchron abgeschlossen wird.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Mesequendcersourcetopologyaktualisierte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353198"
---
# <a name="mesequencersourcetopologyupdated-event"></a>Mesequendcersourcetopologyaktualisierte-Ereignis

Wird von der Sequencer-Quelle ausgelöst, wenn die [**IMF sequencersource:: updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) -Methode asynchron abgeschlossen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE            | BESCHREIBUNG                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UI4<br/> | Der Sequencer-Element Bezeichner der Topologie, die aktualisiert wird. Die Anwendung gibt diesen Wert im *dwID* -Parameter der [**updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) -Methode an.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis signalisiert, dass die Sequencer-Quelle die Topologie aktualisiert hat, bedeutet jedoch nicht, dass die Topologie für die Wiedergabe bereit ist. Die Anwendung sollte auf das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) warten.

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

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 




