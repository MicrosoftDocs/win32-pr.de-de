---
description: Führt einen Schreib-und Lesevorgang für den smartcardbefehl (Application Protocol Data Unit) aus.
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Iscard:: Transaction-Methode (scardmgr. h)'
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
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356861"
---
# <a name="iscardtransaction-method"></a>Iscard:: Transaction-Methode

\[Die **Transaktions** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Transaktions** Methode führt einen Schreib-und Lesevorgang für den [*smartcardbefehl*](../secgloss/s-gly.md) ([*Application Protocol Data Unit*](../secgloss/a-gly.md)) aus. Die Antwort Zeichenfolge von der Smartcard für die Befehls Zeichenfolge, die auf der Karte definiert ist, die an die Smartcard gesendet wurde, kann nach der Rückgabe dieser Funktion aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Ein Zeiger auf das Smartcard-Befehls Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *ppcmd* -Parameter ist ungültig.<br/>           |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppcmd* übergeben.<br/>          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Der Arbeitsspeicher zum erfüllen der Anforderung ist nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie einen Schreib-und Lesevorgang für das Smartcard-Befehls Objekt ausführen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attachbyhandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Attachbyreader**](iscard-attachbyreader.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**\_ATR erhalten**](iscard-get-atr.md)
</dt> <dt>

[**\_cardhandle erhalten**](iscard-get-cardhandle.md)
</dt> <dt>

[**\_Kontext erhalten**](iscard-get-context.md)
</dt> <dt>

[**get- \_ Protokoll**](iscard-get-protocol.md)
</dt> <dt>

[**\_Status erhalten**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Sperrkarte**](iscard-lockscard.md)
</dt> <dt>

[**Erneut**](iscard-reattach.md)
</dt> <dt>

[**Unlockcard**](iscard-unlockscard.md)
</dt> </dl>

 

 
