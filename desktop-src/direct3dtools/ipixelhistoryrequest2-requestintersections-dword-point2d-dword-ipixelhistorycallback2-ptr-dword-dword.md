---
description: Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame verursachen.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2::RequestIntersections-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df5a2301f3eef654b22bc81faab855535b69633a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623166"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections-Methode

Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame verursachen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*frameNumber*   
Der angegebene Frame.

*Pixel*   
Das angegebene Pixel.

*renderTargetPtr*   
Die Adresse des angegebenen Renderziels.

*requestCallback*   
Die Adresse des Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixelHistoryRequest2**](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
