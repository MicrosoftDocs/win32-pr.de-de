---
description: Rückruf zum Zurückgeben von Aufruf Liste-Daten.
MS-HAID: vspixengine.ICallStackCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Icallstackcallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AF380634-A284-4DCA-B746-FB1D8BE099B4
api_name:
- ICallStackCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6b2aa72008d11891c211512308290a3393ee49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746760"
---
# <a name="span-idvspixengineicallstackcallbackspanicallstackcallback-interface"></a><span data-ttu-id="e4099-103"><span id="vspixengine.icallstackcallback"></span>Icallstackcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e4099-103"><span id="vspixengine.icallstackcallback"></span>ICallStackCallback interface</span></span>

<span data-ttu-id="e4099-104">Rückruf zum Zurückgeben von Aufruf Liste-Daten.</span><span class="sxs-lookup"><span data-stu-id="e4099-104">Callback to return callstack data.</span></span>

## <a name="members"></a><span data-ttu-id="e4099-105">Member</span><span class="sxs-lookup"><span data-stu-id="e4099-105">Members</span></span>

<span data-ttu-id="e4099-106">Die **icallstackcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4099-106">The **ICallStackCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e4099-107">**Icallstackcallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4099-107">**ICallStackCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e4099-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e4099-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e4099-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="e4099-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e4099-110">Die **icallstackcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e4099-110">The **ICallStackCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e4099-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e4099-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e4099-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4099-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e4099-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e4099-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e4099-114">Eine Rückruffunktion, die verwendet wird, um den Host über die aufrufstackinformationen zu Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="e4099-114">A callback function used to notify the host of call stack information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e4099-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4099-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e4099-116">Header</span><span class="sxs-lookup"><span data-stu-id="e4099-116">Header</span></span></p></td><td><span data-ttu-id="e4099-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e4099-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
