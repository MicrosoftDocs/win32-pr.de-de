---
description: Die User \_ Auth-Methode ermöglicht den Zugriff auf Benutzerauthentifizierungsdienste.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: ISCardAuth::User_Auth-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a4d4d626507fdcd476cd28267d6366b32ae63e42e7f58488b095db867c430fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015300"
---
# <a name="iscardauthuser_auth-method"></a>ISCardAuth::User \_ Auth-Methode

\[Die **User \_ Auth-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **User \_ Auth-Methode** ermöglicht den Zugriff auf Benutzerauthentifizierungsdienste.

## <a name="syntax"></a>Syntax


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lAlgorID* \[ In\]
</dt> <dd>

Algorithmus, der im Authentifizierungsprozess verwendet werden soll.

</dd> <dt>

*pParam* \[ In\]
</dt> <dd>

Ein [**IByteBuffer-Objekt,**](ibytebuffer.md) das herstellerspezifische Parameter des Authentifizierungsprozesses enthält.

</dd> <dt>

*pBuffer* \[ In\]
</dt> <dd>

Daten, die im Authentifizierungsprozess verwendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardAuth**](iscardauth.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes [](../secgloss/s-gly.md) gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
