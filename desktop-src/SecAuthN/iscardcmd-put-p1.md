---
description: Legt das erste P1-Byte (Parameter) der Anwendungsprotokolldateneinheit (Application Protocol Data Unit, APDU) fest.
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: ISCardCmd::p ut_P1-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7375a04928cf58dc9ef73b6463f2c7d2b19144649e21d7b3220f981584f4c63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008143"
---
# <a name="iscardcmdput_p1-method"></a>ISCardCmd::p ut \_ P1-Methode

\[Die **Put \_ P1-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **put \_ P1-Methode** legt das erste P1-Byte (Parameter) der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ In\]
</dt> <dd>

Das Byte, das das Feld P1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *byP1-Parameter* ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Rufen Sie get P2 auf, um den [**\_ P2-Wert**](iscardcmd-get-p2.md)der APDU festzulegen.

Um die vorhandenen P1-, P2- und P3-Werte abzurufen, rufen [**Sie get \_ P1**](iscardcmd-get-p1.md)auf, [**rufen Sie \_ P2**](iscardcmd-get-p2.md) oder [**\_ P3**](iscardcmd-get-p3.md) ab.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie sie das erste P1-Byte (Parameter) der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) festlegen. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_P1 abrufen**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P2 abrufen**](iscardcmd-get-p2.md)
</dt> <dt>

[**\_P3 abrufen**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**\_put P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
