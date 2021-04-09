---
description: Ein Rückruf, der den Host von Frame Puffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframebuffercallback:: resultCallback-Methode'
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
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124616"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Iframebuffercallback:: resultCallback-Methode

Ein Rückruf, der den Host von Frame Puffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.

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

*Framezahl*   
Die Rahmennummer.

*Breite*   
Die Breite des Frames.

*Flugh*   
Die Höhe des Frames.

*rendertargetptr*   
Das Renderziel, von dem die Ergebnisse stammen. Es ist immer ein Slot, der von der Frame Puffer Anforderung angegeben wird, oder wenn es sich nicht um einen Draw-Befehl handelt, springt der erste RTV-Befehl zur Ausgabe Quelle.

*frameduraction*   
Nicht verwendet.

*Größe*   
Die Größe des Ausgabepuffers in Bytes.

*count5- \_ Puffer*   
Der Inhalt des Renderziels im \_ unorm-Format R8G8B8A8.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iframebuffercallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
