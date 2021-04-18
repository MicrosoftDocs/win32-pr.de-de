---
description: Die get \_ Event-Methode ruft einen Teilnehmer \_ Ereignis Deskriptor für den Ereignistyp ab, der aufgetreten ist.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Itparticipvorgänger Vent:: get_Event-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371288"
---
# <a name="itparticipanteventget_event-method"></a>Itparticipvorgänger Vent:: get- \_ Ereignismethode

\[**get \_ Das Ereignis** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Event** -Methode ruft einen [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor für den Ereignistyp ab, der aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pparticipvorgänger Vent* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor des Ereignisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>      |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pparticipvorgänger Vent* -Parameter ist kein gültiger Zeiger.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itparticipvorgänger Vent**](itparticipantevent.md)
</dt> <dt>

[**Teilnehmer \_ Ereignis**](participant-event.md)
</dt> </dl>

 

 




