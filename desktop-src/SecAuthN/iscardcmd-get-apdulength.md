---
description: Bestimmt die Länge der Anwendungsprotokolldateneinheit (Application Protocol Data Unit, APDU) in Bytes.
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: ISCardCmd::get_ApduLength-Methode (Ddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: be2dc0ed209f4d7be5c36be25579c69149c554ab159590339297b4180f461062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577740"
---
# <a name="iscardcmdget_apdulength-method"></a>ISCardCmd::get \_ ApduLength-Methode

\[Die **\_ get ApduLength-Methode** ist für die Verwendung in den betriebssystemspezifischen Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **get \_ ApduLength-Methode** bestimmt die Länge der [*Anwendungsprotokolldateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) in Bytes.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plSize* \[ out\]
</dt> <dd>

Zeiger auf die Länge der APDU.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *plSize-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *plSize* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Hinweise

Rufen Sie [**get \_ Apdu**](iscardcmd-get-apdu.md)auf, um die unformatierte [*Anwendungsprotokolldateneinheit*](../secgloss/a-gly.md) (APDU) aus dem Bytepuffer abzurufen, der über einen **IStream** zugeordnet ist, der die APDU-Nachricht enthält.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardCmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie die Länge der [*Anwendungsprotokolldateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) abgerufen wird. Im Beispiel wird davon ausgegangen, dass pISCardCmd ein gültiger Zeiger auf eine Instanz der [**ISCardCmd-Schnittstelle**](iscardcmd.md) ist.


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
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

[**get \_ Apdu**](iscardcmd-get-apdu.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
