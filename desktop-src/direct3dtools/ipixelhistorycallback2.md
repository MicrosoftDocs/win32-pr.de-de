---
description: Rückruf zum Zurückgeben von Pixel Verlaufs interabschnitten (Draw-Anruf Ebene) und primitiven (Dreiecks Ebene) in zwei unterschiedlichen Ergebnissen.
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
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521560"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2-Schnittstelle

Rückruf zum Zurückgeben von Pixel Verlaufs interabschnitten (Draw-Anruf Ebene) und primitiven (Dreiecks Ebene) in zwei unterschiedlichen Ergebnissen.

## <a name="members"></a>Member

Die **IPixelHistoryCallback2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IPixelHistoryCallback2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPixelHistoryCallback2** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>Intersectionscallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über Schnittstellen Informationen des Pixel Verlaufs benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>Primitivescallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über die primitiven Vorgangs Informationen des Pixel Verlaufs benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
