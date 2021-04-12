---
description: Wird von der Medien Sitzung ausgelöst, wenn sich der Status einer Topologie ändert.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Mesessiontopologystatus-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959301"
---
# <a name="mesessiontopologystatus-event"></a>Mesessiontopologystatus-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn sich der Status einer Topologie ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                            | BESCHREIBUNG                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Status der MF- \_ Ereignis \_ Topologie \_**](mf-event-topology-status-attribute.md)<br/> | Gibt den neuen Status der Topologie an.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Ein Codebeispiel, in dem der [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Zeiger aus dem-Ereignis abgerufen wird, finden Sie unter [mesessiontopologyset](mesessiontopologyset.md) -Ereignis.

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

 

 




