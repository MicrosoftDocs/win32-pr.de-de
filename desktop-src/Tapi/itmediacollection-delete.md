---
description: Die Delete-Methode löscht die Medien, die dem angegebenen Index entsprechen.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ITMediaCollection::D elete-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31f799ae413c26e09552d02a8ed31412ae25330acd7060cfad1d03a29741eee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864829"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection::D elete-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Delete-Methode** löscht die Medien, die dem angegebenen Index entsprechen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index der zu löschenden Medien.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                                              | Beschreibung                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                     | Methode war erfolgreich.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | Der *Index-Parameter* hat einen Wert kleiner als 1 oder größer als die aktuelle Anzahl von Elementen.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                            | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/>                                          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                                   | Interner Fehler (sollte nur auftreten, wenn ein vorheriger Aufruf einen Fehler zurückgegeben hat).<br/>                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                                | Diese Methode ist noch nicht implementiert.<br/>                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ ERROR \_ CODE(SDPBLB \_ CONF \_ BLOB \_ DESTROYED)**</dt> </dl> | Das SDP-Blob ist nicht vorhanden.<br/>                                                                   |



 

## <a name="remarks"></a>Hinweise

Die meisten C- und C++-Listen sind 0-basiert, aber dieser Index basiert aus Visual Basic Kompatibilität auf 1, was bedeutet, dass das erste Element eine Indexnummer von 1 hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




