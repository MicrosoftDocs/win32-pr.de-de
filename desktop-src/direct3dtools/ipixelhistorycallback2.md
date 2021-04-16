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
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="e791f-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e791f-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="e791f-104">Rückruf zum Zurückgeben von Pixel Verlaufs interabschnitten (Draw-Anruf Ebene) und primitiven (Dreiecks Ebene) in zwei unterschiedlichen Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="e791f-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="e791f-105">Member</span><span class="sxs-lookup"><span data-stu-id="e791f-105">Members</span></span>

<span data-ttu-id="e791f-106">Die **IPixelHistoryCallback2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e791f-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e791f-107">**IPixelHistoryCallback2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e791f-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="e791f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e791f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e791f-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="e791f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e791f-110">Die **IPixelHistoryCallback2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e791f-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e791f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e791f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e791f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e791f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e791f-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>Intersectionscallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e791f-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e791f-114">Ein Rückruf, der den Host über Schnittstellen Informationen des Pixel Verlaufs benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e791f-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e791f-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>Primitivescallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e791f-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e791f-116">Ein Rückruf, der den Host über die primitiven Vorgangs Informationen des Pixel Verlaufs benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e791f-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e791f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e791f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e791f-118">Header</span><span class="sxs-lookup"><span data-stu-id="e791f-118">Header</span></span></p></td><td><span data-ttu-id="e791f-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e791f-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
