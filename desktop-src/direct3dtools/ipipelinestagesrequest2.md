---
description: '<span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2-Schnittstelle: Nicht verwendet. Früher war eine Anforderung für Pipelinestufendaten.'
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107068"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="14e69-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="14e69-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="14e69-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="14e69-105">Not used.</span></span> <span data-ttu-id="14e69-106">Früher war eine Anforderung für Pipelinestufendaten.</span><span class="sxs-lookup"><span data-stu-id="14e69-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="14e69-107">Member</span><span class="sxs-lookup"><span data-stu-id="14e69-107">Members</span></span>

<span data-ttu-id="14e69-108">Die **IPipeLineStagesRequest2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="14e69-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="14e69-109">**IPipeLineStagesRequest2** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="14e69-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="14e69-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="14e69-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="14e69-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="14e69-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="14e69-112">Die **IPipeLineStagesRequest2-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="14e69-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="14e69-113">Methode</span><span class="sxs-lookup"><span data-stu-id="14e69-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="14e69-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14e69-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="14e69-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="14e69-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="14e69-116">Eine asynchrone Anforderung zum Abruf von Compute-Shaderdaten für die angegebene Dispatch.</span><span class="sxs-lookup"><span data-stu-id="14e69-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="14e69-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="14e69-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="14e69-118">Eine asynchrone Anforderung, um zu erhalten, ob die Compute-Shaderstufe für den angegebenen Frame und das angegebene Ereignis verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="14e69-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="14e69-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14e69-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="14e69-120">Header</span><span class="sxs-lookup"><span data-stu-id="14e69-120">Header</span></span></p></td><td><span data-ttu-id="14e69-121">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="14e69-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
