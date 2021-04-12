---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames aufgezeichnet wurden.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframelistcallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482662"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>Iframelistcallback:: resultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames aufgezeichnet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a>Parameter

*numFrames*   
Die Anzahl der aufgezeichneten Frames.

*count0 \_ frameNum*   
Die Frame Nummern der aufgezeichneten Frames.

*count0 \_ frameeventids*   
Das abschließende Ereignis, das jedem Frame zugeordnet ist.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iframelistcallback**](/windows/desktop/direct3dtools/iframelistcallback)

 

 
