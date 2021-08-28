---
description: Fordert an, eine Shaderdebugsitzung für die angegebene Pipelinephase, ggf. Pixel/Scheitelpunkt, Ereignis und Frame zu starten.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest::BeginDebugShader-Methode
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
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629854"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader-Methode

Fordert an, eine Shaderdebugsitzung für die angegebene Pipelinephase, ggf. Pixel/Scheitelpunkt, Ereignis und Frame zu starten.

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

*errorCallback*   
Die Adresse eines Rückrufs für Fehler, die während des Debuggens auftreten können.

*Eventid*   
Das angegebene Ereignis.

*frameNumber*   
Der angegebene Frame.

*Scheitelpunkt*   
Der angegebene Scheitelpunkt. Gilt nur beim Debuggen eines Vertex-Shaders.

*Pixel*   
Das angegebene Pixel. Gilt nur beim Debuggen eines Pixel-Shaders.

*Bühne*   
Die angegebene Pipelinephase.

*pPixelHistory*   
Die Adresse der Pixelverlaufsergebnisse, die zum Suchen des zugeordneten zu debuggende Pixels verwendet werden. Gilt nur beim Debuggen eines Pixel-Shaders.

*pDevice*   
Die Adresse, die an die Debug-Engine für die Kommunikation mit dieser Debugsitzung übergeben werden soll (debug engine readprocessmemory für diese Adresse).

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
