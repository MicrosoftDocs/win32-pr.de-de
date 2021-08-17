---
description: Setzt den aktuellen Sicherheitskontext der Smartcard zurück.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: ISCardVerify::ResetSecurityState-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6cf1d27298e5bc37288b209547e82f29cfba1393dc3c654563977fbd3f0bf0ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141063"
---
# <a name="iscardverifyresetsecuritystate-method"></a>ISCardVerify::ResetSecurityState-Methode

\[Die **ResetSecurityState-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ResetSecurityState-Methode** setzt den aktuellen [*Sicherheitskontext*](../secgloss/s-gly.md) der [*Smartcard*](../secgloss/s-gly.md)zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Um den [*Sicherheitskontext*](../secgloss/s-gly.md) ohne Zurücksetzen erneut zu aktivieren, rufen [**Sie Entsperren auf.**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardVerify.**](iscardverify.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[**Entsperren**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))
</dt> </dl>

 

 
