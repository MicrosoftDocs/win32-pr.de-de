---
description: Mit der Delete-Methode wird das Medium gelöscht, das dem angegebenen Index entspricht.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: Itmediacollection::D Elete-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372583"
---
# <a name="itmediacollectiondelete-method"></a>Itmediacollection::D Elete-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **Delete** -Methode wird das Medium gelöscht, das dem angegebenen Index entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des zu löschenden Mediums.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                                              | Beschreibung                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                     | Methode war erfolgreich.<br/>                                                                             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                                             | Der *Index* -Parameter weist einen Wert auf, der kleiner als 1 oder größer als die aktuelle Anzahl der Elemente ist.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>                                            | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                                          |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                                                   | Interner Fehler (sollte nur auftreten, wenn ein vorheriger-Rückruf einen Fehler zurückgegeben hat).<br/>                      |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                                                | Diese Methode ist noch nicht implementiert.<br/>                                                           |
| <dl> <dt>**HRESULT \_ aus \_ Fehler \_ Code (sdpblb \_ conf \_ BLOB \_ zerstört)**</dt> </dl> | Das SDP-BLOB ist nicht vorhanden.<br/>                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Die meisten C-und C++-Listen sind 0-basiert, aber dieser Index basiert auf Visual Basic Kompatibilität, d. h., das erste Element hat eine Indexnummer von 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> </dl>

 

 




