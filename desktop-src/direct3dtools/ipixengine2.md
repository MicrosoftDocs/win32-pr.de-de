---
description: Erweiterungen der ursprünglichen ipixengine-Schnittstelle.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481254"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="2e679-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2e679-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="2e679-104">Erweiterungen der ursprünglichen ipixengine-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2e679-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="2e679-105">Member</span><span class="sxs-lookup"><span data-stu-id="2e679-105">Members</span></span>

<span data-ttu-id="2e679-106">Die **IPixEngine2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2e679-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e679-107">**IPixEngine2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e679-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="2e679-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="2e679-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="2e679-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="2e679-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="2e679-110">Die **IPixEngine2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2e679-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="2e679-111">Methode</span><span class="sxs-lookup"><span data-stu-id="2e679-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="2e679-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e679-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2e679-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>Endexperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="2e679-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2e679-114">Beendet das Erlebnis und vervollständigt das Grafik Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2e679-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="2e679-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>Getplaybackmachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="2e679-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2e679-116">Ruft Informationen über den aktuellen Wiedergabe Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2e679-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="2e679-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>Onnewdataavailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="2e679-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2e679-118">Anforderungen, um anzugeben, dass das Grafik Protokoll neue Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="2e679-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="2e679-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>Setplaybackmachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="2e679-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="2e679-120">Legt den aktuellen Wiedergabe Computer für das angegebene Grafik Protokoll fest.</span><span class="sxs-lookup"><span data-stu-id="2e679-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="2e679-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e679-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2e679-122">Header</span><span class="sxs-lookup"><span data-stu-id="2e679-122">Header</span></span></p></td><td><span data-ttu-id="2e679-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2e679-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
