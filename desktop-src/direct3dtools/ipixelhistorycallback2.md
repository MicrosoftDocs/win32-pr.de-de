---
description: Rückruf zum Zurückgeben von Pixelverlaufs-Schnittmengen (Zeichnen-Aufrufebene) und Primitiven (Dreiecksebene) in zwei unterschiedlichen Ergebnissen.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ccb3ea0f3e3cdffbe0b3469b1897d4081eaff89a9ffa4e7eaf43217664f57d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283225"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2-Schnittstelle

Rückruf zum Zurückgeben von Pixelverlaufs-Schnittmengen (Zeichnen-Aufrufebene) und Primitiven (Dreiecksebene) in zwei unterschiedlichen Ergebnissen.

## <a name="members"></a>Member

Die **IPixelHistoryCallback2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixelHistoryCallback2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixelHistoryCallback2-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">Beschreibung</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host von Pixelverlaufs-Schnittpunktinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über primitive Vorgangsinformationen des Pixelverlaufs benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
