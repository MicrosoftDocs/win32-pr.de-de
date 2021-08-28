---
description: '<span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback-Schnittstelle: Nicht verwendet. Früher ein Rückruf für Pipelinestufendaten.'
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback-Schnittstelle
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
ms.openlocfilehash: 2fc828d902f1daa3b2c0c75d2f22671d9bdec942
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787499"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback-Schnittstelle

Nicht verwendet. Früher ein Rückruf für Pipelinestufendaten.

## <a name="members"></a>Members

Die **IPipeLineStagesCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPipeLineStagesCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IPipeLineStagesCallback-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Methode</th><th >BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></td><td ><p>Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen vom Draw-Aufruf der assocaited-Anforderung verwendet werden.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></td><td ><p>Ein Rückruf, der den Host benachrichtigt, von welchen Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgegeben werden können.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></td><td ><p>Ein Rückruf, der den Host der Pipelinestufen-Meshinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></td><td ><p>Ein Rückruf, der den Host der Pipelinestufen bildinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
