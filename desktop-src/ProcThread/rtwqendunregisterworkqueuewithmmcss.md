---
description: Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeitswarteschlange mit einer MMCSS-Aufgabe (Multimedia Class Scheduler Service) ab.
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793400"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>RtwqEndUnregisterWorkQueueWithMMCSS-Funktion

Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeitswarteschlange mit einer MMCSS-Aufgabe (Multimedia Class Scheduler Service) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pResult* 
</dt> <dd>

Zeiger auf die [**INTERFACESAsyncResult-Schnittstelle.**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) Übergeben Sie den gleichen Zeiger, den Ihr Rückrufobjekt in der [**IRtwqAsyncCallback::Invoke-Methode**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) empfangen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>        |
| Bibliothek<br/>                  | <dl> <dt>Rtworkq.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
