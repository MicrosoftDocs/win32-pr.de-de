---
description: Rückruf zum Schreiben einer Textur als DDS-Datei.
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Itexturecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 831de15656960cdc72ef2db50c1f3d13b8491e38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747369"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span id="vspixengine.itexturecallback"></span>Itexturecallback-Schnittstelle

Rückruf zum Schreiben einer Textur als DDS-Datei.

## <a name="members"></a>Member

Die **itexturecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itexturecallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **itexturecallback** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über den benachrichtigt. Die DDS-Datei (DirectDraw Surface) mit Ergebnissen aus der zugeordneten Anforderung ist bereit.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
