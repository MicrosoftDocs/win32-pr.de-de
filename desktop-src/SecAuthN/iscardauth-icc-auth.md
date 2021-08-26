---
description: Mit der METHODE FÜR DIE \_ Authentifizierung kann eine Anwendung die Smartcard authentifizieren.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: ISCardAuth::ICC_Auth-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b96d40d6c35250b55b6aa2bb37733492fda874df0346b24c859431d749a3e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015380"
---
# <a name="iscardauthicc_auth-method"></a>\_ISCardAuth::ICC-Authentifizierungsmethode

\[Die **\_ VERFAHRENAuthentifizierungsmethode** ist für die Verwendung in den betriebssystemspezifischen Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Mit der METHODE FÜR DIE **\_ Authentifizierung** kann eine Anwendung die Smartcard authentifizieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
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

Ein [**IByteBuffer-Objekt,**](ibytebuffer.md) das anbieterspezifische Parameter des Authentifizierungsprozesses enthält.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

Enthält bei der Eingabe Daten, die im Authentifizierungsprozess verwendet werden sollen.

Enthält in der Ausgabe das Ergebnis des Authentifizierungsprozesses.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 
