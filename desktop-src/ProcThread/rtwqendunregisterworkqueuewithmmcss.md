---
description: Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeits Warteschlange bei einem Multimedia Class Scheduler Service-Task (MMCSS) ab.
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Rtwqendunregisterworkqueuewithmmcss-Funktion
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
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865736"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Rtwqendunregisterworkqueuewithmmcss-Funktion

Schließt eine asynchrone Anforderung zum Aufheben der Registrierung einer Arbeits Warteschlange bei einem Multimedia Class Scheduler Service-Task (MMCSS) ab.

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

Zeiger auf die [**imfasynkresult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle. Übergeben Sie denselben Zeiger, den das Rückruf Objekt in der Methode " [**untwqasynccallback:: Aufrufen**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) " erhalten hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>None</dt> </dl>        |
| Bibliothek<br/>                  | <dl> <dt>Rtworkq. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
