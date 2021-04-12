---
description: Rückruf von Engine, der angibt, dass die Verarbeitung neuer Frames, die dem Protokoll hinzugefügt wurden, abgeschlossen ist.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Inewframescallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392866"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="d9c8e-103"><span id="vspixengine.inewframescallback"></span>Inewframescallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d9c8e-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="d9c8e-104">Rückruf von Engine, der angibt, dass die Verarbeitung neuer Frames, die dem Protokoll hinzugefügt wurden, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="d9c8e-105">Member</span><span class="sxs-lookup"><span data-stu-id="d9c8e-105">Members</span></span>

<span data-ttu-id="d9c8e-106">Die **inewframescallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d9c8e-107">In " **inewframescallback** " sind auch folgende Typen von Membern verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d9c8e-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d9c8e-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d9c8e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d9c8e-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="d9c8e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d9c8e-110">Die **inewframescallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d9c8e-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d9c8e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d9c8e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9c8e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d9c8e-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>Abbrechen</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9c8e-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d9c8e-114">Ein Rückruf, der den Host benachrichtigt, dass alle Anforderungen abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d9c8e-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>Cancelusingcallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9c8e-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d9c8e-116">Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d9c8e-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>Cancelusingcookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9c8e-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d9c8e-118">Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem er ein Cookie verwendet, das die Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d9c8e-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>Newframesavailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9c8e-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d9c8e-120">Ein Rückruf, der den Host benachrichtigt, dass neue Frames zur Verarbeitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d9c8e-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d9c8e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9c8e-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d9c8e-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9c8e-122">Header</span></span></p></td><td><span data-ttu-id="d9c8e-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d9c8e-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
