---
description: Anforderung von Pixelverlaufs-Schnittpunkten und Primitiven separat.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4643c993dc1cd5dc7aee6a8d325de7fb53a6c69e
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787306"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2-Schnittstelle

Anforderung von Pixelverlaufs-Schnittpunkten und Primitiven separat.

## <a name="members"></a>Members

Die **IPixelHistoryRequest2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixelHistoryRequest2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixelHistoryRequest2-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Methode</th><th >BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></td><td ><p>Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame verursachen.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></td><td ><p>Fordert eine Liste von Primitiven von einer bestimmten Schnittmenge an. Weitere Informationen finden Sie in der RequestIntersections-Memberfunktion.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
