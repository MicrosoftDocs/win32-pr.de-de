---
description: Rückruf zum Zurückgeben eines Renderziels. Das Format des zurückgegebenen \_ Renderziels ist R8G8B8A8 unorm, unabhängig vom Format des in-Engine-renderTarget.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iframebuffercallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392665"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="0527f-104"><span id="vspixengine.iframebuffercallback"></span>Iframebuffercallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0527f-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="0527f-105">Rückruf zum Zurückgeben eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="0527f-105">Callback to return a render target.</span></span> <span data-ttu-id="0527f-106">Das Format des zurückgegebenen \_ Renderziels ist R8G8B8A8 unorm, unabhängig vom Format des in-Engine-renderTarget.</span><span class="sxs-lookup"><span data-stu-id="0527f-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="0527f-107">Member</span><span class="sxs-lookup"><span data-stu-id="0527f-107">Members</span></span>

<span data-ttu-id="0527f-108">Die **iframebuffercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0527f-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0527f-109">**Iframebuffercallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0527f-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0527f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0527f-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0527f-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="0527f-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0527f-112">Die **iframebuffercallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0527f-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0527f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0527f-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0527f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0527f-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0527f-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0527f-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0527f-116">Ein Rückruf, der den Host von Frame Puffer-Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0527f-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0527f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0527f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0527f-118">Header</span><span class="sxs-lookup"><span data-stu-id="0527f-118">Header</span></span></p></td><td><span data-ttu-id="0527f-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0527f-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
