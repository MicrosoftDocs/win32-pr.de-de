---
description: Ruft den Bezeichner des Protokolls ab, das derzeit auf der Smartcard verwendet wird.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: ISCard::get_Protocol-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f59522f9ec5f22976874aff225d73fc44e8e0cfa8f06022e22312ab8bd80858
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482160"
---
# <a name="iscardget_protocol-method"></a>\_ISCard::get-Protokollmethode

\[Die **get \_ Protocol-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **get \_ Protocol-Methode** ruft den Bezeichner des Protokolls ab, das derzeit auf der [*Smartcard*](../secgloss/s-gly.md)verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pProtocol* \[ out\]
</dt> <dd>

Zeiger auf den Protokollbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operation erfolgreich abgeschlossen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *pProtocol-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | Ein ungültiger Zeiger wurde in *pProtocol* übergeben.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen des Bezeichners des Protokolls, das derzeit auf der Smartcard verwendet wird.


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
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

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**get \_ Context**](iscard-get-context.md)
</dt> <dt>

[**\_Get Status**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
