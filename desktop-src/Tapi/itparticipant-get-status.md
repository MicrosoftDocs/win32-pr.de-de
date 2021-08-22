---
description: Die get \_ Status-Methode gibt eine \_ VARIANT-BOOL zurück, die den Teilnehmerstatus angibt.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: ITParticipant::get_Status-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1585c9605447e7b515885ecf9e30d060afb7a57d14c5b29a66025f2df9da05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060848"
---
# <a name="itparticipantget_status-method"></a>ITParticipant::get \_ Status-Methode

\[**get \_ Der** Status ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **get \_ Status-Methode** gibt eine \_ VARIANT-BOOL zurück, die den Teilnehmerstatus angibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pITStream* \[ In\]
</dt> <dd>

Zeiger auf [**die ITStream-Schnittstelle.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> <dt>

*pStatus* \[ out\]
</dt> <dd>

VARIANT \_ TRUE, wenn der Teilnehmer für den Stream aktiviert ist, VARIANT \_ FALSE, wenn er deaktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Methode nicht implementiert.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>           |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *pITStream-Parameter* ist kein gültiger Zeiger.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pITStream-Parameter* ist kein Zeiger auf eine gültige Schnittstelle.<br/> |



 

## <a name="remarks"></a>Hinweise

Durch das Aktivieren oder Deaktivieren des Status eines Teilnehmers in einem Stream kann eine Anwendung einen bestimmten Teilnehmer im Wesentlichen stummschalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**put \_ Status**](itparticipant-put-status.md)
</dt> </dl>

 

