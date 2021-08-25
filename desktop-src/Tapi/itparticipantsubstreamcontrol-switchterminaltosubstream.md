---
description: Die SwitchTerminalToSubStream-Methode legt ein Terminal auf den Teilnehmerunterstream fest.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: ITParticipantSubStreamControl::SwitchTerminalToSubStream-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f211d4f3ff0f01801fb5497d36d81fa46e43397d8b69227180b022c9e74a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774650"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>ITParticipantSubStreamControl::SwitchTerminalToSubStream-Methode

\[**SwitchTerminalToSubStream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SwitchTerminalToSubStream-Methode** legt ein Terminal auf den Teilnehmerunterstream fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pITTerminal* \[ In\]
</dt> <dd>

Zeiger auf [**die ITTerminal-Schnittstelle.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)

</dd> <dt>

*pITSubStream* \[ In\]
</dt> <dd>

Zeiger auf [**die ITSubStream-Schnittstelle.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                     | Beschreibung                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                                                       |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>    | Auf Teilnehmerinformationen für den Stream konnte nicht zugegriffen werden.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Der *pParticipant-Parameter* oder *der pITSubStream-Parameter* verweisen nicht auf eine gültige Schnittstelle.<br/> |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Der Unterstream ist nicht bereit.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/>                                    |



 

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
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

