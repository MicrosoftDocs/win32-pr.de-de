---
description: Nicht verwendet. Früher ein Rückruf, der auf &\# 0034 antwortet; Frame&\# 0034;-Ereignis erfassen.
MS-HAID: vspixengine.IRunActionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ununaktioncallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A597D33C-A5CD-48D4-94E2-4C28F510AC78
api_name:
- IRunActionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc14e0cc6be088e85af086dba3423e3a2e374ed5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481246"
---
# <a name="span-idvspixengineirunactioncallbackspanirunactioncallback-interface"></a><span data-ttu-id="cf668-104"><span id="vspixengine.irunactioncallback"></span>Ununaktioncallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cf668-104"><span id="vspixengine.irunactioncallback"></span>IRunActionCallback interface</span></span>

<span data-ttu-id="cf668-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf668-105">Not used.</span></span> <span data-ttu-id="cf668-106">Früher ein Rückruf, der auf das Ereignis "Capture Frame" antwortet.</span><span class="sxs-lookup"><span data-stu-id="cf668-106">Formerly a callback to respond to "capture frame" event.</span></span>

## <a name="members"></a><span data-ttu-id="cf668-107">Member</span><span class="sxs-lookup"><span data-stu-id="cf668-107">Members</span></span>

<span data-ttu-id="cf668-108">Die **ununaktioncallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cf668-108">The **IRunActionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cf668-109">Bei " **ununaktioncallback** " sind auch diese Typen von Membern aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cf668-109">**IRunActionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="cf668-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="cf668-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="cf668-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="cf668-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="cf668-112">Die **ununaktioncallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cf668-112">The **IRunActionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="cf668-113">Methode</span><span class="sxs-lookup"><span data-stu-id="cf668-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="cf668-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf668-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="cf668-115"><a href="/windows/desktop/direct3dtools/irunactioncallback-requestresult-iunknown-ptr"><strong>"RequestResult"</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf668-115"><a href="/windows/desktop/direct3dtools/irunactioncallback-requestresult-iunknown-ptr"><strong>RequestResult</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="cf668-116">Eine Rückruffunktion, die verwendet wird, um den Host über Ergebnisse einer Aktion zu benachrichtigen (z. b. einen Frame erfassen), die er angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="cf668-116">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="cf668-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf668-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cf668-118">Header</span><span class="sxs-lookup"><span data-stu-id="cf668-118">Header</span></span></p></td><td><span data-ttu-id="cf668-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cf668-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
