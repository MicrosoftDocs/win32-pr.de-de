---
description: Fordert zum Starten einer shaderdebugsitzung für die angegebene Pipeline Phase, Pixel/Scheitelpunkt, falls zutreffend, Ereignis und Frame.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Idebugshaderrequest:: begindebugshader-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124633"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Idebugshaderrequest:: begindebugshader-Methode

Fordert zum Starten einer shaderdebugsitzung für die angegebene Pipeline Phase, Pixel/Scheitelpunkt, falls zutreffend, Ereignis und Frame.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Parameter

*errorcallback*   
Die Adresse eines Rückrufs für Fehler, die während des Debuggens auftreten können.

*EventID*   
Das angegebene Ereignis.

*Framezahl*   
Der angegebene Frame.

*Vertex*   
Der angegebene Scheitelpunkt. Gilt nur, wenn ein Vertexshader debuggt wird.

*Megapixel*   
Das angegebene Pixel. Gilt nur beim Debuggen eines Pixelshaders.

*inszeniert*   
Die angegebene Pipeline Phase.

*ppixelhistory*   
Die Adresse der Pixel Verlaufs Ergebnisse, die zum Suchen des zugeordneten Pixels zum Debuggen verwendet werden. Gilt nur beim Debuggen eines Pixelshaders.

*pdevice*   
Die Adresse, die an die Debug-Engine für die Kommunikation mit dieser Debugsitzung übergeben werden soll (Debugmodul-lesenprozessspeicher für diese Adresse).

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Idebugshaderrequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
