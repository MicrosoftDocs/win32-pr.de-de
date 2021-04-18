---
description: Mit der get \_ substreamfromparticipants-Methode kann eine Anwendung ermitteln, welche Substreams einem bestimmten Teilnehmer zugeordnet sind.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Itparticipantsubstreamcontrol:: get_SubStreamFromParticipant-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364493"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>Itparticipantsubstreamcontrol:: get \_ substreamfromparticipants-Methode

\[**get \_ Substreamfromteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **get \_ substreamfromparticipants** -Methode kann eine Anwendung ermitteln, welche Substreams einem bestimmten Teilnehmer zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pteilnehmer* \[ in\]
</dt> <dd>

Zeiger auf die [**itparticipants**](itparticipant.md) -Schnittstelle.

</dd> <dt>

*ppitsubstream* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                                 |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppitsubstream* -Parameter ist kein gültiger Zeiger.<br/>             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pparticipants* -Parameter verweist nicht auf eine gültige Schnittstelle.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>  | Auf die Teilnehmer Informationen des Streams konnte nicht zugegriffen werden.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itparticipantsubstreamcontrol**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**Itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

