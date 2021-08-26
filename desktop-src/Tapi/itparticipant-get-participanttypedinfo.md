---
description: Die get ParticipantTypedInfo-Methode ruft eine BSTR-Darstellung des Typs der erforderlichen Informationen ab, z. B. \_ PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: ITParticipant::get_ParticipantTypedInfo-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43afb80b0f1161cf0060c8492576ade4f682af44cb4b2dbb13ab49d2c65aab66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867150"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>ITParticipant::get \_ ParticipantTypedInfo-Methode

\[**get \_ ParticipantTypedInfo** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ ParticipantTypedInfo-Methode** ruft **eine BSTR-Darstellung** des Typs der erforderlichen Informationen ab, z. B. PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ In\]
</dt> <dd>

[**TEILNEHMER \_ TYPED \_ INFO-Deskriptor**](participant-typed-info.md) des erforderlichen Informationstyps.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Zeiger auf **die BSTR-Darstellung** der erforderlichen Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                    | Beschreibung                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>         | Storage von Informationen in *ppInfo* ist fehlgeschlagen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Der *InfoType-Parameter* ist ungültig.<br/>               |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>      | Der *ppInfo-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**TAPI \_ E \_ NOITEM**</dt> </dl> | TAPI enthält keine Informationen zum angegebenen Typ.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den für den *ppInfo-Parameter* zugeordneten Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**VOM \_ TEILNEHMER TYPIERTE \_ INFORMATIONEN**](participant-typed-info.md)
</dt> <dt>

[**Medientypen**](tapimediatype--constants.md)
</dt> </dl>

 

