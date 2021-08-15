---
description: Die get \_ Participant-Methode ruft einen Zeiger auf ein Array von ITParticipant-Schnittstellen ab, die die am Ereignis beteiligten Teilnehmer darstellen.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: ITParticipantEvent::get_Participant-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d53b5269b0940888ca5a849e4ecc8cc98d053bbe80340dcfa1a858eabd6ceed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864514"
---
# <a name="itparticipanteventget_participant-method"></a>ITParticipantEvent::get \_ Participant-Methode

\[**get \_ Der** Teilnehmer ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **methode \_ get Participant** ruft einen Zeiger auf ein Array von [**ITParticipant-Schnittstellen**](itparticipant.md) ab, die die am Ereignis beteiligten Teilnehmer darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppParticipant* \[ out\]
</dt> <dd>

Zeiger auf ein Array von [**ITParticipant-Schnittstellen.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                           | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>  |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Dem Ereignis sind keine Teilnehmer zugeordnet.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>       | Der *ppParticipant-Parameter* ist kein gültiger Zeiger.<br/> |



 

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

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




