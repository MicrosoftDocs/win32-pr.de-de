---
description: Nicht verwendet.
MS-HAID: vspixengine.IStatusCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Istatus Callback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C082689B-C322-4CF9-9623-1755DB4D02DC
api_name:
- IStatusCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a053873694890bd96b6b24857995622ff511b03
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342939"
---
# <a name="span-idvspixengineistatuscallbackspanistatuscallback-interface"></a><span data-ttu-id="30f26-103"><span id="vspixengine.istatuscallback"></span>Istatus Callback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="30f26-103"><span id="vspixengine.istatuscallback"></span>IStatusCallback interface</span></span>

<span data-ttu-id="30f26-104">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30f26-104">Not used.</span></span>

## <a name="members"></a><span data-ttu-id="30f26-105">Member</span><span class="sxs-lookup"><span data-stu-id="30f26-105">Members</span></span>

<span data-ttu-id="30f26-106">Die **istatus Callback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="30f26-106">The **IStatusCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="30f26-107">**Istatus Callback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="30f26-107">**IStatusCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="30f26-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="30f26-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="30f26-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="30f26-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="30f26-110">Die **istatus Callback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="30f26-110">The **IStatusCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="30f26-111">Methode</span><span class="sxs-lookup"><span data-stu-id="30f26-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="30f26-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30f26-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="30f26-113"><a href="/windows/desktop/direct3dtools/istatuscallback-status-dword-dword-dword"><strong>Status</strong></a></span><span class="sxs-lookup"><span data-stu-id="30f26-113"><a href="/windows/desktop/direct3dtools/istatuscallback-status-dword-dword-dword"><strong>Status</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="30f26-114">Eine Rückruffunktion, die verwendet wird, um den Host über den Fortschritt der Engine zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="30f26-114">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="30f26-115">Dadurch kann der Host auch feststellen, dass die Engine weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30f26-115">This also serves as a way for the host to determine that the engine is still running.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="30f26-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30f26-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="30f26-117">Header</span><span class="sxs-lookup"><span data-stu-id="30f26-117">Header</span></span></p></td><td><span data-ttu-id="30f26-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="30f26-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
