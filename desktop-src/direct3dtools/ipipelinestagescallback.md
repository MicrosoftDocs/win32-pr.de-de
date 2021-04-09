---
description: Nicht verwendet. Früher ein Rückruf für Daten der Pipeline Stufen.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipipelinestagescallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860490"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>Ipipelinestagescallback-Schnittstelle

Nicht verwendet. Früher ein Rückruf für Daten der Pipeline Stufen.

## <a name="members"></a>Member

Die **ipipelinestagescallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipipelinestagescallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **ipipelinestagescallback** -Schnittstelle verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>Getsupportedstages</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen vom zeichnen-Befehl der assocaas-Anforderung verwendet werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>Meshdatanotavailablecallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>Meshdatavertcallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host der Bild Informationen von Pipeline Stufen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
