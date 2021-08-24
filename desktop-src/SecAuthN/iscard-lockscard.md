---
description: Die LockSCard-Methode beansprucht exklusiven Zugriff auf die Smartcard.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: ISCard::LockSCard-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bdb9e531013836bb193719faa7bcd9d73581e83a3599bd51439be27c44ba1e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482170"
---
# <a name="iscardlockscard-method"></a>ISCard::LockSCard-Methode

\[Die **LockSCard-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **LockSCard-Methode** beansprucht exklusiven Zugriff auf die [*Smartcard*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                          | Beschreibung                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operation erfolgreich abgeschlossen.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zum oben aufgeführten COM-Fehlercode kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

Um die Smartcard zu entsperren, rufen Sie die [**ISCard::UnlockSCard-Methode**](iscard-unlockscard.md) auf.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt den Erwerb des exklusiven Zugriffs auf die Smartcard.


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
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

[**ISCard**](iscard.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
