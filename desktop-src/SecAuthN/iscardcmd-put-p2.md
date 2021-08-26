---
description: Legt das zweite Parameter-Byte (P2) in der Anwendungsprotokolldateneinheit (Application Protocol Data Unit, APDU) fest.
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: ISCardCmd::p ut_P2-Methode (Mouseddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a66ef756d65e4cc011e6a5e4797a8ccae690dd404b6f25f1f9a7d3bbb2826069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014580"
---
# <a name="iscardcmdput_p2-method"></a>ISCardCmd::p ut \_ P2-Methode

\[Die **put \_ P2-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **put \_ P2-Methode** legt das zweite Parameter byte (P2) in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP2* \[ In\]
</dt> <dd>

Das Byte, das das P2-Feld ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *byP2-Parameter* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Um den P1-Wert des APDU festzulegen, rufen Sie [**\_ put P1**](iscardcmd-put-p1.md)auf.

Um die vorhandenen P1-, P2- und P3-Werte abzurufen, rufen [**Sie get \_ P1**](iscardcmd-get-p1.md)auf, [**rufen Sie \_ P2**](iscardcmd-get-p2.md) oder [**\_ P3**](iscardcmd-get-p3.md) ab.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie das zweite P2-Byte (Parameter) der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) festgelegt wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_P1 abrufen**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P2 abrufen**](iscardcmd-get-p2.md)
</dt> <dt>

[**\_P3 abrufen**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**\_put P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
