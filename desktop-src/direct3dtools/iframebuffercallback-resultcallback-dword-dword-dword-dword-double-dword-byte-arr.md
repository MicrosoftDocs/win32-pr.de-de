---
description: Ein Rückruf, der den Host über framebuffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback::ResultCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2308ec5355da8f8fda7eeccf31d1cbe19e8a8247
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626676"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback-Methode

Ein Rückruf, der den Host über framebuffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Parameter

*frameNumber*   
Die Framenummer.

*Breite*   
Die Breite des Frames.

*Höhe*   
Die Höhe des Rahmens.

*renderTargetPtr*   
Das Renderziel, von dem die Ergebnisse stammen. Es handelt sich immer um einen Slot, der von der Framepufferanforderung angegeben wird, oder, wenn kein Draw-Aufruf, dann der erste RTV-Bount an die Ausgabequelle.

*frameDuraction*   
Nicht verwendet.

*Größe*   
Die Größe des Ausgabepuffers in Bytes.

*\_count5-Puffer*   
Der Inhalt des Renderziels im UNORM-Format R8G8B8A8. \_

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
