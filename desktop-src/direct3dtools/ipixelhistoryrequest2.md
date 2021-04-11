---
description: Eine separate Anforderung für Pixel Verlaufs interabschnitte und primitive.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789829d85f4cb986de694470a8cebddf3f26675
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342108"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span data-ttu-id="ab802-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ab802-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2 interface</span></span>

<span data-ttu-id="ab802-104">Eine separate Anforderung für Pixel Verlaufs interabschnitte und primitive.</span><span class="sxs-lookup"><span data-stu-id="ab802-104">Request for pixel history intersections and primitives separately.</span></span>

## <a name="members"></a><span data-ttu-id="ab802-105">Member</span><span class="sxs-lookup"><span data-stu-id="ab802-105">Members</span></span>

<span data-ttu-id="ab802-106">Die **IPixelHistoryRequest2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ab802-106">The **IPixelHistoryRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab802-107">**IPixelHistoryRequest2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab802-107">**IPixelHistoryRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="ab802-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="ab802-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ab802-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="ab802-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ab802-110">Die **IPixelHistoryRequest2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ab802-110">The **IPixelHistoryRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ab802-111">Methode</span><span class="sxs-lookup"><span data-stu-id="ab802-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ab802-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab802-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ab802-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>Requestinterabschnitts</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab802-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ab802-114">Fordert eine Liste von Ereignissen an, die eine Änderung im angegebenen Pixel, Renderziel/UAV und Frame auslösen.</span><span class="sxs-lookup"><span data-stu-id="ab802-114">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ab802-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>Requestprimitives</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab802-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ab802-116">Fordert eine Liste von primitiven aus einer bestimmten Schnittmenge an.</span><span class="sxs-lookup"><span data-stu-id="ab802-116">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="ab802-117">Weitere Informationen finden Sie unter der requestinterabschnitts-Member-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ab802-117">For more information, see the RequestIntersections member function.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ab802-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab802-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ab802-119">Header</span><span class="sxs-lookup"><span data-stu-id="ab802-119">Header</span></span></p></td><td><span data-ttu-id="ab802-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ab802-120">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
