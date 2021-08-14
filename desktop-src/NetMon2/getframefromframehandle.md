---
description: Die GetFrameFromFrameHandle-Funktion gibt einen Zeiger auf einen Frame von einem Framehandle zurück.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: GetFrameFromFrameHandle-Funktion (Netmon.h)
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
ms.openlocfilehash: 56ee96fd04d4860648dac2ec6b20a537ba420beb070c8f9b7248d9e3b4acd184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366544"
---
# <a name="getframefromframehandle-function"></a>GetFrameFromFrameHandle-Funktion

Die **GetFrameFromFrameHandle-Funktion** gibt einen Zeiger auf einen Frame von einem Framehandle zurück.

## <a name="syntax"></a>Syntax


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Hinweise

Die **GetFrameFromFrameHandle-Funktion** ruft Daten ab, die nicht von den anderen Hilfsfunktionen abgerufen werden können, die Netzwerkmonitor werden. Verwenden Sie nach Möglichkeit die folgenden Funktionen.

<dl>

[**GetFrameDstAddressOffset**](getframedstaddressoffset.md)  
[**GetFrameSrcAddressOffset**](getframesrcaddressoffset.md)  
[**GetFrameCaptureHandle**](getframecapturehandle.md)  
[**GetFrameDestAddress**](getframedestaddress.md)  
[**GetFrameSourceAddress**](getframesourceaddress.md)  
[**GetFrameMacHeaderLength**](getframemacheaderlength.md)  
[**GetFrameLength**](getframelength.md)  
[**GetFrameStoredLength**](getframestoredlength.md)  
[**GetFrameMacType**](getframemactype.md)  
[**GetFrameNumber**](getframenumber.md)  
[**GetFrameTimeStamp**](getframetimestamp.md)  
</dl>

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameFromFrameHandle-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




