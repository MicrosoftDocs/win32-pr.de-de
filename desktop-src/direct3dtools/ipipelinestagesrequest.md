---
description: Nicht verwendet. Zuvor eine Anforderung für Daten der Pipeline Stufen.
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipipelinestagesrequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4dfa67e0770b1c709ee80bffd01831859ad4c45a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342560"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="14d2f-104"><span id="vspixengine.ipipelinestagesrequest"></span>Ipipelinestagesrequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="14d2f-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="14d2f-105">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="14d2f-105">Not used.</span></span> <span data-ttu-id="14d2f-106">Zuvor eine Anforderung für Daten der Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="14d2f-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="14d2f-107">Member</span><span class="sxs-lookup"><span data-stu-id="14d2f-107">Members</span></span>

<span data-ttu-id="14d2f-108">Die **ipipelinestagesrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="14d2f-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="14d2f-109">**Ipipelinestagesrequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14d2f-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="14d2f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="14d2f-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="14d2f-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="14d2f-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="14d2f-112">Die **ipipelinestagesrequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="14d2f-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="14d2f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="14d2f-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="14d2f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14d2f-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="14d2f-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>Requestasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="14d2f-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="14d2f-116">Eine asynchrone Anforderung zum erhalten von Vorschaubildern für das Fenstergrafik Pipeline Stufen.</span><span class="sxs-lookup"><span data-stu-id="14d2f-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="14d2f-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>Requestsupportedstagesasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="14d2f-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="14d2f-118">Eine asynchrone Anforderung zum erhalten einer Liste von Stufen, die für den angegebenen Frame und das angegebene Ereignis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14d2f-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="14d2f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14d2f-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="14d2f-120">Header</span><span class="sxs-lookup"><span data-stu-id="14d2f-120">Header</span></span></p></td><td><span data-ttu-id="14d2f-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="14d2f-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
