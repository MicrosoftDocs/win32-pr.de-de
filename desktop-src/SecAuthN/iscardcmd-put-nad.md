---
description: Gibt die Knotenadresse (Eigenschaft) an, die mit der ISCardCmd-Schnittstelle verwendet werden soll.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: ISCardCmd::p ut_Schriftmethode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 84ade2e2ca69c328650f4c7df485814e4eaacedf3fdb0190fc883cde864a8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481390"
---
# <a name="iscardcmdput_nad-method"></a>ISCardCmd::p ut-Methode \_

\[Die **\_ put-Methode steht** für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **\_ put-Methode gibt** die Knotenadresse (Eigenschaft) an, die mit der [**ISCardCmd-Schnittstelle verwendet werden**](iscardcmd.md) soll. Dies gilt nur für die Kommunikation mit [*dem T=1-Protokoll.*](../secgloss/t-gly.md) Standardmäßig verwendet das [**ISCardCmd-Objekt**](iscardcmd.md) einen Wert von 0 (null).

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bNad* \[ In\]
</dt> <dd>

Byte, das die zu verwendende Beimeine darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *bNad-Parameter* ist ungültig.<br/>    |



 

## <a name="remarks"></a>Hinweise

Diese Methode sollte nur aufgerufen werden, wenn es erforderlich ist, einen anderen Wert als 0 (null) für das -System zu verwenden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine Knotenadresse angeben, die mit der [**ISCardCmd-Schnittstelle verwendet werden**](iscardcmd.md) soll. Im Beispiel wird davon ausgegangen, dass byNadValue eine Variable vom Typ **BYTE** ist, der zuvor ein Wert zugewiesen wurde, und dass pISCardCmd ein gültiger Zeiger auf eine Instanz der **ISCardCmd-Schnittstelle** ist.


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
