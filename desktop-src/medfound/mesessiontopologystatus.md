---
description: Wird von der Mediensitzung ausgelöst, wenn sich der Status einer Topologie ändert.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: MESessionTopologyStatus-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42adfd1a86319f65077e87925eb23807253f12b06e977ee1eb9e494a4c7df180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723720"
---
# <a name="mesessiontopologystatus-event"></a>MESessionTopologyStatus-Ereignis

Wird von der Mediensitzung ausgelöst, wenn sich der Status einer Topologie ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | Beschreibung                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESTopology-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) der Topologie.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                            | Beschreibung                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**STATUS \_ DER MF-EREIGNISTOPOLOGIE \_ \_**](mf-event-topology-status-attribute.md)<br/> | Gibt den neuen Status der Topologie an.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Ein Codebeispiel, das den [**POINTERTopology-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) aus dem -Ereignis abruft, finden Sie unter [MESessionTopologySet-Ereignis.](mesessiontopologyset.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




