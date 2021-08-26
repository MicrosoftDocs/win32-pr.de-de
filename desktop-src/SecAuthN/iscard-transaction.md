---
description: Führt einen Schreib- und Lesevorgang für das Smartcardbefehlsobjekt (Anwendungsprotokoll-Dateneinheit) aus.
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: ISCard::Transaction-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 60f5be785da0cca6aac4fdf1c098d49548696420042ce60a97a46de73edde9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015560"
---
# <a name="iscardtransaction-method"></a>ISCard::Transaction-Methode

\[Die **Transaction-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Transaction-Methode** führt einen Schreib- und Lesevorgang für das [*Smartcardbefehlsobjekt*](../secgloss/s-gly.md) [*(Anwendungsprotokoll-Dateneinheit)*](../secgloss/a-gly.md)aus. Auf die Antwortzeichenfolge von der Smartcard für die Befehlszeichenfolge, die in der an die Smartcard gesendeten Karte definiert ist, kann nach der Rückgabe dieser Funktion zugegriffen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Ein Zeiger auf das Smartcard-Befehlsobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *ppCmd-Parameter* ist ungültig.<br/>           |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppCmd übergeben.*<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Der Arbeitsspeicher zum Erfüllen der Anforderung ist nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Ausführung eines Schreib- und Lesevorgang für das Smartcard-Befehlsobjekt.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
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
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**Get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**Get \_ Context**](iscard-get-context.md)
</dt> <dt>

[**\_get-Protokoll**](iscard-get-protocol.md)
</dt> <dt>

[**Status \_ "get"**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Anfügen**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
