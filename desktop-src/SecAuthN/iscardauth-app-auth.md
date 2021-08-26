---
description: Die \_ APP-Authentifizierungsmethode authentifiziert die Anwendung. Es ermöglicht einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Abfrage-/Signaturprotokolls), wenn die Authentifizierung von einer Smartcard angefordert wird.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: ISCardAuth::APP_Auth-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: db6d2b673caf15d5d15e63894a6c5a589fd2d18ea031a3201a562f255ee6cf2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015550"
---
# <a name="iscardauthapp_auth-method"></a>\_ISCardAuth::APP-Authentifizierungsmethode

\[Die **\_ APP-Authentifizierungsmethode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ APP-Authentifizierungsmethode** authentifiziert die Anwendung. Es ermöglicht einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Abfrage-/Signaturprotokolls), wenn die Authentifizierung von einer [*Smartcard*](../secgloss/s-gly.md)angefordert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lAlgoID* \[ In\]
</dt> <dd>

Algorithmus, der im Authentifizierungsprozess verwendet werden soll.

</dd> <dt>

*pParam* \[ In\]
</dt> <dd>

Ein [**IByteBuffer**](ibytebuffer.md) mit anbieterspezifischen Parametern des Authentifizierungsprozesses.

</dd> <dt>

*pBuffer* \[ In\]
</dt> <dd>

Für die Berechnung erforderliche Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardAuth**](iscardauth.md).

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

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
