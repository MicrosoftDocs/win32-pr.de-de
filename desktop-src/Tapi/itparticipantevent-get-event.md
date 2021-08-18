---
description: Die get \_ Event-Methode ruft einen PARTICIPANT \_ EVENT-Deskriptor des Ereignistyps ab, der aufgetreten ist.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: ITParticipantEvent::get_Event-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864701"
---
# <a name="itparticipanteventget_event-method"></a>ITParticipantEvent::get \_ Event-Methode

\[**get \_ Das Ereignis** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ Event-Methode** ruft einen [**PARTICIPANT EVENT-Deskriptor \_**](participant-event.md) des Ereignistyps ab, der aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pParticipantEvent* \[ out\]
</dt> <dd>

Zeiger auf einen [**PARTICIPANT EVENT-Deskriptor \_**](participant-event.md) des Ereignisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>      |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *pParticipantEvent-Parameter* ist kein gültiger Zeiger.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**\_TEILNEHMEREREIGNIS**](participant-event.md)
</dt> </dl>

 

 




