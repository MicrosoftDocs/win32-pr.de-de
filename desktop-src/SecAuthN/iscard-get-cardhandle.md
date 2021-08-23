---
description: Ruft das Handle für eine verbundene Smartcard ab. Diese Methode gibt ( \* pHandle) == NULL zurück, wenn keine Verbindung besteht.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: ISCard::get_CardHandle-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8a01b7c4531b82c154b6c6e04c1cf0fb5fa2003729e8abf5c0af39470a171bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482230"
---
# <a name="iscardget_cardhandle-method"></a>ISCard::get \_ CardHandle-Methode

\[Die **Get \_ CardHandle-Methode** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **get \_ CardHandle-Methode** ruft das Handle für eine verbundene [*Smartcard ab.*](../secgloss/s-gly.md) Diese Methode gibt ( \* pHandle) == **NULL zurück,** wenn keine Verbindung besteht.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pHandle* \[ out\]
</dt> <dd>

Zeiger auf das Kartenhandles bei der Rückgabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *pHandle-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    | Ein fehlerhafter Zeiger wurde in *pHandle übergeben.*<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen des Smartcardhandles.


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**Get \_ Context**](iscard-get-context.md)
</dt> <dt>

[**\_get-Protokoll**](iscard-get-protocol.md)
</dt> <dt>

[**Status \_ "get"**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
