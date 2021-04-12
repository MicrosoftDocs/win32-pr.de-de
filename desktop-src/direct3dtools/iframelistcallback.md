---
description: Rückruf, der die Liste der Frames mit der Ereignis-ID und der Rahmennummer zurückgibt.
MS-HAID: vspixengine.IFrameListCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iframelistcallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 16318DBE-4126-4331-B726-DCF929F712DA
api_name:
- IFrameListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a4fe281584a9ca51d18eee22f7e9fd4a92e48f88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392873"
---
# <a name="span-idvspixengineiframelistcallbackspaniframelistcallback-interface"></a><span data-ttu-id="c5c66-103"><span id="vspixengine.iframelistcallback"></span>Iframelistcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c5c66-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback interface</span></span>

<span data-ttu-id="c5c66-104">Rückruf, der die Liste der Frames mit der Ereignis-ID und der Rahmennummer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c5c66-104">Callback to return the list of frames with their event id and frame number.</span></span>

## <a name="members"></a><span data-ttu-id="c5c66-105">Member</span><span class="sxs-lookup"><span data-stu-id="c5c66-105">Members</span></span>

<span data-ttu-id="c5c66-106">Die **iframelistcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c5c66-106">The **IFrameListCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c5c66-107">**Iframelistcallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5c66-107">**IFrameListCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c5c66-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="c5c66-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c5c66-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="c5c66-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c5c66-110">Die **iframelistcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c5c66-110">The **IFrameListCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c5c66-111">Methode</span><span class="sxs-lookup"><span data-stu-id="c5c66-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c5c66-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5c66-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c5c66-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5c66-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c5c66-114">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c5c66-114">A callback function used to notify the host of which frames were captured.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c5c66-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5c66-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c5c66-116">Header</span><span class="sxs-lookup"><span data-stu-id="c5c66-116">Header</span></span></p></td><td><span data-ttu-id="c5c66-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c5c66-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
