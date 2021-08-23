---
description: Ruft das zweite Parameter-Byte (P2) aus der Anwendungsprotokoll-Dateneinheit (Application Protocol Data Unit, APDU) ab.
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: ISCardCmd::get_P2-Methode (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf9d5735e4583e0b55a91e6c45f9f23905bd199e15697596a93b06c2347aab65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577550"
---
# <a name="iscardcmdget_p2-method"></a>ISCardCmd::get \_ P2-Methode

\[Die **Get \_ P2-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **get \_ P2-Methode** ruft das zweite Parameter-Byte (P2) aus der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbyP2* \[ out\]
</dt> <dd>

Zeiger auf das Byte, bei dem es sich um das P2 aus der APDU handelt, bei der Rückgabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *pbyP2-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *pbyP2 übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Um den P2-Parameter auf einen neuen Wert zu setzen, rufen Sie [**put \_ P2 auf.**](iscardcmd-put-p2.md)

Um die P1- oder P3-Parameter zu erhalten, rufen Sie [**get \_ P1 bzw.**](iscardcmd-get-p1.md) [**get \_ P3**](iscardcmd-get-p3.md) auf.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes [](../secgloss/s-gly.md) gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie das zweite Parameter-Byte (P2) aus der [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) abgerufen wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_P1-Get**](iscardcmd-get-p1.md)
</dt> <dt>

[**\_P3-Get**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
