---
description: Eine Rückruffunktion, die verwendet wird, um den Host über die aufrufstackinformationen zu Benachrichtigen
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Icallstackcallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860307"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>Icallstackcallback:: resultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über die aufrufstackinformationen zu Benachrichtigen

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a>Parameter

*Countdown*   
Die Anzahl der zurückgegebenen Aufruf Liste-Framebuffers.

*count0 \_ callstackframebuffer*   
Die Aufruf Liste-Informationen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Icallstackcallback**](/windows/desktop/direct3dtools/icallstackcallback)

 

 
