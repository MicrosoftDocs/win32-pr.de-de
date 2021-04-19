---
description: Mit der switchterminalto substream-Methode wird ein Terminal auf den Teilnehmer teilstream festgelegt.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Itparticipantsubstreamcontrol:: switchterminalto substream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374029"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>Itparticipantsubstreamcontrol:: switchterminalto substream-Methode

\[**Switchterminalto substream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **switchterminalto substream** -Methode wird ein Terminal auf den Teilnehmer teilstream festgelegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitterminal* \[ in\]
</dt> <dd>

Zeiger auf die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle.

</dd> <dt>

*pitsubstream* \[ in\]
</dt> <dd>

Zeiger auf die [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                     | Beschreibung                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                                                       |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>    | Der Zugriff auf Teilnehmer Informationen für den Stream war nicht möglich.<br/>                           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>    | Der *pparticipants* -oder der *pitsubstream* -Parameter verweist nicht auf eine gültige Schnittstelle.<br/> |
| <dl> <dt>**TAPI \_ E \_ noItems**</dt> </dl> | Der unter Datenstrom ist nicht bereit.<br/>                                                             |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>                                    |



 

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
</dt> <dt>

[**Itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

