---
description: Nicht verwendet. Früher ein Rückruf für Daten der Pipeline Stufen.
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
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957832"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="7d1b8-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7d1b8-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="7d1b8-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-105">Not used.</span></span> <span data-ttu-id="7d1b8-106">Früher ein Rückruf für Daten der Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="7d1b8-107">Member</span><span class="sxs-lookup"><span data-stu-id="7d1b8-107">Members</span></span>

<span data-ttu-id="7d1b8-108">Die **IPipeLineStagesCallback2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7d1b8-109">**IPipeLineStagesCallback2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d1b8-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="7d1b8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7d1b8-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="7d1b8-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="7d1b8-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="7d1b8-112">Die **IPipeLineStagesCallback2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="7d1b8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7d1b8-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="7d1b8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d1b8-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="7d1b8-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>Threaddatadimensioncallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d1b8-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7d1b8-116">Ein Rückruf, der den Host über die Anzahl der Threads und Gruppen des Compute-Shaders in der zugeordneten Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="7d1b8-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>Threaddatanotavailablecallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d1b8-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7d1b8-118">Ein Rückruf, der den Host benachrichtigt, dass threaddata für eine bestimmte Pipeline Phase und ein bestimmtes Ereignis nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7d1b8-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="7d1b8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d1b8-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7d1b8-120">Header</span><span class="sxs-lookup"><span data-stu-id="7d1b8-120">Header</span></span></p></td><td><span data-ttu-id="7d1b8-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7d1b8-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
