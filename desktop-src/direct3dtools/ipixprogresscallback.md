---
description: Rückruf von Engine, um den Fortschritt zurückzugeben.
MS-HAID: vspixengine.IPixProgressCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixprogresscallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B2DAF90B-5615-464F-84F9-A80912E09FB9
api_name:
- IPixProgressCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: afb3e962569b1871282577f3d46618374b59425f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339669"
---
# <a name="span-idvspixengineipixprogresscallbackspanipixprogresscallback-interface"></a><span data-ttu-id="0f9fb-103"><span id="vspixengine.ipixprogresscallback"></span>Ipixprogresscallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0f9fb-103"><span id="vspixengine.ipixprogresscallback"></span>IPixProgressCallback interface</span></span>

<span data-ttu-id="0f9fb-104">Rückruf von Engine, um den Fortschritt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-104">Callback from engine to return progress.</span></span>

## <a name="members"></a><span data-ttu-id="0f9fb-105">Member</span><span class="sxs-lookup"><span data-stu-id="0f9fb-105">Members</span></span>

<span data-ttu-id="0f9fb-106">Die **ipixprogresscallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-106">The **IPixProgressCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0f9fb-107">**Ipixprogresscallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0f9fb-107">**IPixProgressCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0f9fb-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0f9fb-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0f9fb-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="0f9fb-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0f9fb-110">Die **ipixprogresscallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-110">The **IPixProgressCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0f9fb-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0f9fb-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0f9fb-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f9fb-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0f9fb-113"><a href="/windows/desktop/direct3dtools/ipixprogresscallback-progress-dword-dword"><strong>Fortschritt</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f9fb-113"><a href="/windows/desktop/direct3dtools/ipixprogresscallback-progress-dword-dword"><strong>Progress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0f9fb-114">Ein Rückruf, der den Host über den Fortschritt einer zugeordneten Anforderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="0f9fb-114">A callback that notifies the host of the progress of an associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0f9fb-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f9fb-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0f9fb-116">Header</span><span class="sxs-lookup"><span data-stu-id="0f9fb-116">Header</span></span></p></td><td><span data-ttu-id="0f9fb-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0f9fb-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
