---
description: Mit der get \_ participantfromsubstream-Methode kann eine Anwendung ermitteln, welche Teilnehmer mit einem bestimmten substream verknüpft sind.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Itparticipantsubstreamcontrol:: get_ParticipantFromSubStream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352031"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>Itparticipantsubstreamcontrol:: get \_ participantfromsubstream-Methode

\[**get \_ "Participantfromsubstream** " ist für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **get \_ participantfromsubstream** -Methode kann eine Anwendung ermitteln, welche Teilnehmer mit einem bestimmten substream verknüpft sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitsubstream* \[ in\]
</dt> <dd>

Zeiger auf die [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstelle.

</dd> <dt>

*ppteilnehmer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                     | Beschreibung                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                                       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>       | Der Parameter " *pitsubstream* " oder " *ppparticipants* " ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>    | Der Parameter " *pitsubstream* " verweist nicht auf eine gültige Schnittstelle.<br/>         |
| <dl> <dt>**TAPI \_ E \_ noItems**</dt> </dl> | Dem substream sind keine Teilnehmer zugeordnet.<br/>                |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                    |



 

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

 

