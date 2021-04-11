---
description: Die lockscard-Methode beansprucht exklusiven Zugriff auf die Smartcard.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'Iscard:: lockscard-Methode (scardmgr. h)'
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
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217763"
---
# <a name="iscardlockscard-method"></a>Iscard:: lockscard-Methode

\[Die **lockscard** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **lockscard** -Methode beansprucht exklusiven Zugriff auf die [*Smartcard*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                          | Beschreibung                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operation erfolgreich abgeschlossen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zum oben aufgeführten com-Fehlercode gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

Um die Smartcard zu entsperren, wenden Sie die [**iscard:: unlockscard**](iscard-unlockscard.md) -Methode an.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie exklusiven Zugriff auf die Smartcard erwerben.


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

[**Iscard**](iscard.md)
</dt> <dt>

[**Unlockcard**](iscard-unlockscard.md)
</dt> </dl>

 

 
