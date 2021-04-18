---
description: Die getframefromframehandle-Funktion gibt einen Zeiger auf einen Frame aus einem Frame Handle zurück.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Getframefromframehandle-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344403"
---
# <a name="getframefromframehandle-function"></a>Getframefromframehandle-Funktion

Die **getframefromframehandle** -Funktion gibt einen Zeiger auf einen Frame aus einem Frame Handle zurück.

## <a name="syntax"></a>Syntax


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

Die **getframefromframehandle** -Funktion Ruft Daten ab, die von den anderen von Netzwerkmonitor bereitgestellten Hilfsfunktionen nicht abgerufen werden können. Verwenden Sie nach Möglichkeit die folgenden Funktionen.

<dl>

[**Getframedstaddressoffset**](getframedstaddressoffset.md)  
[**Getframesrcaddressoffset**](getframesrcaddressoffset.md)  
[**Getframecapturehandle**](getframecapturehandle.md)  
[**Getframeumstaddress**](getframedestaddress.md)  
[**Getframesourceaddress**](getframesourceaddress.md)  
[**Getframemacheaderlength**](getframemacheaderlength.md)  
[**GetFrameLength**](getframelength.md)  
[**Getframestoredlength**](getframestoredlength.md)  
[**Getframemactype**](getframemactype.md)  
[**Getframennummer**](getframenumber.md)  
[**Getframetimestamp**](getframetimestamp.md)  
</dl>

[*Experten*](e.md) und [*Parser*](p.md) können die **getframefromframehandle** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




