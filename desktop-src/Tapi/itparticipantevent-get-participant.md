---
description: Die get- \_ Teilnehmer Methode erhält einen Zeiger auf ein Array von itparticipants-Schnittstellen, die die am Ereignis beteiligten Teilnehmer darstellen.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Itparticipvorgänger Vent:: get_Participant-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368573"
---
# <a name="itparticipanteventget_participant-method"></a>Itparticipvorgänger Vent:: get- \_ Teilnehmer Methode

\[**get \_ Der Teilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get- \_ Teilnehmer** Methode erhält einen Zeiger auf ein Array von [**itparticipants**](itparticipant.md) -Schnittstellen, die die am Ereignis beteiligten Teilnehmer darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppteilnehmer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                           | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                     |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>  |
| <dl> <dt>**TAPI \_ E \_ noItems**</dt> </dl> | Dem Ereignis sind keine Teilnehmer zugeordnet.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>       | Der *ppparticipants* -Parameter ist kein gültiger Zeiger.<br/> |



 

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

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

 




