---
description: Die Anwendung wird von der APP- \_ Authentifizierungsmethode authentifiziert. Sie ermöglicht es einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Challenge/Signature-Protokolls), wenn die Authentifizierung von einer Smartcard angefordert wird.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Iscardauth:: APP_Auth-Methode'
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
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863532"
---
# <a name="iscardauthapp_auth-method"></a>Iscardauth:: App-Authentifizierungs \_ Methode

\[Die **App \_** -Authentifizierungsmethode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Anwendung wird von der APP-Authentifizierungsmethode authentifiziert. **\_** Sie ermöglicht es einer Anwendung, sich selbst zu authentifizieren (mithilfe eines Challenge/Signature-Protokolls), wenn die Authentifizierung von einer [*Smartcard*](../secgloss/s-gly.md)angefordert wird.

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

*lalgoid* \[ in\]
</dt> <dd>

Der Algorithmus, der beim Authentifizierungsprozess verwendet werden soll.

</dd> <dt>

*pParam* \[ in\]
</dt> <dd>

Ein [**ibytebuffer**](ibytebuffer.md) mit anbieterspezifischen Parametern des Authentifizierungsprozesses.

</dd> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Erforderliche Daten für die Berechnung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardauth**](iscardauth.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardauth**](iscardauth.md)
</dt> <dt>

[**Ibytebuffer**](ibytebuffer.md)
</dt> </dl>

 

 
