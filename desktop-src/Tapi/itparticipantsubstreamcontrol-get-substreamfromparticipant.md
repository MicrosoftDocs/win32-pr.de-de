---
description: Mit der get SubStreamFromParticipant-Methode kann eine Anwendung feststellen, welche \_ Unterstreams einem bestimmten Teilnehmer zugeordnet sind.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: ITParticipantSubStreamControl::get_SubStreamFromParticipant-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40487bbef7e678722a2710d99bce9ed1ebe2f5192705f0a7dc03f86e10e421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621530"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>ITParticipantSubStreamControl::get \_ SubStreamFromParticipant-Methode

\[**get \_ SubStreamFromParticipant** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Mit **der get \_ SubStreamFromParticipant-Methode** kann eine Anwendung feststellen, welche Unterstreams einem bestimmten Teilnehmer zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pParticipant* \[ In\]
</dt> <dd>

Zeiger auf [**die ITParticipant-Schnittstelle.**](itparticipant.md)

</dd> <dt>

*ppITSubStream* \[ out\]
</dt> <dd>

Zeiger auf ein Array von [**ITParticipant-Schnittstellenzeigern.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                 |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *ppITSubStream-Parameter* ist kein gültiger Zeiger.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pParticipant-Parameter* ist kein Zeiger auf eine gültige Schnittstelle.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Auf die Teilnehmerinformationen des Streams konnte nicht zugegriffen werden.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

