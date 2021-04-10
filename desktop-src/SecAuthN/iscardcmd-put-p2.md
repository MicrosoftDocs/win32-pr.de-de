---
description: Legt den zweiten Parameter (P2) in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: Iscardcmd::p ut_P2-Methode (scarddat. h)
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
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214407"
---
# <a name="iscardcmdput_p2-method"></a>Iscardcmd::p UT \_ P2-Methode

\[Die **Put \_ P2** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der **Put \_ P2** -Methode wird der zweite Parameter (P2) in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) festgelegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP2* \[ in\]
</dt> <dd>

Das Byte, das das P2-Feld ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *byP2* -Parameter ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Um den P1-Wert des APDU festzulegen, nennen Sie [**Put \_ P1**](iscardcmd-put-p1.md).

Um die vorhandenen Werte für P1, P2 und P3 abzurufen, rufen [**Sie get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) oder [**get \_ P3**](iscardcmd-get-p3.md) auf.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie das zweite Parameter-Byte (P2) der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) festlegen. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_P1 erhalten**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P2 erhalten**](iscardcmd-get-p2.md)
</dt> <dt>

[**\_P3 erhalten**](iscardcmd-get-p3.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**\_P1 platzieren**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
