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
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="44222-104"><span id="vspixengine.ipipelinestagescallback"></span>Ipipelinestagescallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="44222-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="44222-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44222-105">Not used.</span></span> <span data-ttu-id="44222-106">Früher ein Rückruf für Daten der Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="44222-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="44222-107">Member</span><span class="sxs-lookup"><span data-stu-id="44222-107">Members</span></span>

<span data-ttu-id="44222-108">Die **ipipelinestagescallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="44222-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="44222-109">**Ipipelinestagescallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44222-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="44222-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="44222-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="44222-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="44222-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="44222-112">Die **ipipelinestagescallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="44222-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="44222-113">Methode</span><span class="sxs-lookup"><span data-stu-id="44222-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="44222-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44222-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="44222-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>Getsupportedstages</strong></a></span><span class="sxs-lookup"><span data-stu-id="44222-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="44222-116">Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen vom zeichnen-Befehl der assocaas-Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44222-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="44222-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>Meshdatanotavailablecallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="44222-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="44222-118">Ein Rückruf, der den Host darüber benachrichtigt, welche Pipeline Stufen keine Mesh-Daten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="44222-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="44222-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>Meshdatavertcallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="44222-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="44222-120">Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44222-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="44222-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="44222-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="44222-122">Ein Rückruf, der den Host der Bild Informationen von Pipeline Stufen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44222-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="44222-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44222-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="44222-124">Header</span><span class="sxs-lookup"><span data-stu-id="44222-124">Header</span></span></p></td><td><span data-ttu-id="44222-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="44222-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
