---
description: Die GetCügge-Methode gibt eine Herausforderung von der Smartcard zurück.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: ISCardAuth::GetChallenge-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0132ab8b4b3b2f646639c1618a9f2ca7e67fad1ce2c2fcec38590c7608802091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015420"
---
# <a name="iscardauthgetchallenge-method"></a>ISCardAuth::GetChallenge-Methode

\[Die **GetChallenge-Methode** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **GetCügge-Methode** gibt eine Herausforderung von der [*Smartcard zurück.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lAlgoID* \[ in, optional\]
</dt> <dd>

Algorithmus, der im Authentifizierungsprozess verwendet werden soll.

</dd> <dt>

*lLengthOfCbigge* \[ In\]
</dt> <dd>

Maximale Länge der erwarteten Antwort.

</dd> <dt>

*pParam* \[ In\]
</dt> <dd>

Ein [**IByteBuffer-Objekt,**](ibytebuffer.md) das herstellerspezifische Parameter des Authentifizierungsprozesses enthält.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

Zeigt bei der Eingabe auf den Puffer.

Enthält in der Ausgabe die Challenge-Daten von der Karte.

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

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

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
</dt> </dl>

 

 
