---
description: Nicht verwendet. Zuvor eine Anforderung für Daten der Pipeline Stufen.
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
ms.openlocfilehash: 9d344b7e128adf344f50a99ba41a420ca794baec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123986"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="f67d5-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f67d5-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="f67d5-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f67d5-105">Not used.</span></span> <span data-ttu-id="f67d5-106">Zuvor eine Anforderung für Daten der Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="f67d5-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="f67d5-107">Member</span><span class="sxs-lookup"><span data-stu-id="f67d5-107">Members</span></span>

<span data-ttu-id="f67d5-108">Die **IPipeLineStagesRequest2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f67d5-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f67d5-109">**IPipeLineStagesRequest2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f67d5-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="f67d5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f67d5-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f67d5-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="f67d5-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f67d5-112">Die **IPipeLineStagesRequest2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f67d5-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f67d5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="f67d5-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f67d5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f67d5-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f67d5-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>Requestcomputeshaderdataasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="f67d5-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f67d5-116">Eine asynchrone Anforderung zum Aufrufen von Compute-shaderdaten für die angegebene Verteilung.</span><span class="sxs-lookup"><span data-stu-id="f67d5-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f67d5-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>Requestcomputeshaderstageasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="f67d5-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f67d5-118">Eine asynchrone Anforderung, um zu erhalten, ob die Compute-Shader-Phase für den angegebenen Frame und das angegebene Ereignis verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f67d5-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f67d5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f67d5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f67d5-120">Header</span><span class="sxs-lookup"><span data-stu-id="f67d5-120">Header</span></span></p></td><td><span data-ttu-id="f67d5-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f67d5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
