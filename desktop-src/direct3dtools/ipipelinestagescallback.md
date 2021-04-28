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
ms.openlocfilehash: 7782985f4317a02d2b159722f7a5897978b952b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087898"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="f05f2-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f05f2-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="f05f2-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f05f2-105">Not used.</span></span> <span data-ttu-id="f05f2-106">Früher ein Rückruf für Pipelinestufendaten.</span><span class="sxs-lookup"><span data-stu-id="f05f2-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="f05f2-107">Member</span><span class="sxs-lookup"><span data-stu-id="f05f2-107">Members</span></span>

<span data-ttu-id="f05f2-108">Die **IPipeLineStagesCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="f05f2-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f05f2-109">**IPipeLineStagesCallback** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="f05f2-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f05f2-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f05f2-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f05f2-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="f05f2-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f05f2-112">Die **IPipeLineStagesCallback-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f05f2-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f05f2-113">Methode</span><span class="sxs-lookup"><span data-stu-id="f05f2-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f05f2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f05f2-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f05f2-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="f05f2-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f05f2-116">Ein Rückruf, der den Host benachrichtigt, welche Pipelinestufen vom Zeichnen-Aufruf der assocaited-Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f05f2-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f05f2-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f05f2-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f05f2-118">Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen keine Meshdaten für das in der zugeordneten Anforderung angegebene Ereignis zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="f05f2-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f05f2-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f05f2-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f05f2-120">Ein Rückruf, der den Host der Pipelinestufen Gitternetzinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f05f2-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f05f2-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f05f2-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f05f2-122">Ein Rückruf, der den Host der Pipelinestufen-Bildinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f05f2-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f05f2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f05f2-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f05f2-124">Header</span><span class="sxs-lookup"><span data-stu-id="f05f2-124">Header</span></span></p></td><td><span data-ttu-id="f05f2-125">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="f05f2-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
