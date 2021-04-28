---
description: '<span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2-Schnittstelle: Nicht verwendet. Früher ein Rückruf für Pipelinestufendaten.'
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 941a056a5c2af00cfa1bb53f038cbeb923a777bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097388"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2-Schnittstelle

Nicht verwendet. Früher ein Rückruf für Pipelinestufendaten.

## <a name="members"></a>Member

Die **IPipeLineStagesCallback2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPipeLineStagesCallback2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPipeLineStagesCallback2-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host über die Anzahl der Threads und Gruppen des Compute-Shaders in der zugeordneten Anforderung benachrichtigt.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></td><td style="text-align: left;"><p>Ein Rückruf, der den Host benachrichtigt, dass ThreadData für eine bestimmte Pipelinephase und ein bestimmtes Pipelineereignis nicht verfügbar ist.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
