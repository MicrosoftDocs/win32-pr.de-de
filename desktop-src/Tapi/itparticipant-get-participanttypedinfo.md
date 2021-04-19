---
description: Die \_ Methode Get participanttyetdinfo erhält eine BSTR-Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Itteilnehmer:: get_ParticipantTypedInfo-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356359"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>Itteilnehmer:: get \_ participanttypdinfo-Methode

\[**get \_ "Participanttypeer** " ist für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode **get \_ participanttyetdinfo** erhält eine **BSTR** -Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Deskriptor des Typs der benötigten Informationen.

</dd> <dt>

*ppinfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die **BSTR** -Darstellung der benötigten Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                    | Beschreibung                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>         | Fehler beim Speichern von Informationen in *ppinfo* .<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *InfoType* -Parameter ist ungültig.<br/>               |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>      | Der *ppinfo* -Parameter ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**TAPI \_ E \_ noitem**</dt> </dl> | TAPI weist keine Informationen zum angegebenen Typ auf.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>  | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppinfo* -Parameter zugewiesenen Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**\_typisierte Teilnehmer \_ Informationen**](participant-typed-info.md)
</dt> <dt>

[**Medientypen**](tapimediatype--constants.md)
</dt> </dl>

 

