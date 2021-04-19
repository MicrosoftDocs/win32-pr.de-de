---
description: Rückruf zum Zurückgeben der Anweisungen, die beim Erstellen einer shaderablaufverfolgung generiert wurden.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Idebugshadercallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 676d76a0dbc199880badebc904a4eb66d2ad4d0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346401"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span data-ttu-id="64289-103"><span id="vspixengine.idebugshadercallback"></span>Idebugshadercallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64289-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback interface</span></span>

<span data-ttu-id="64289-104">Rückruf zum Zurückgeben der Anweisungen, die beim Erstellen einer shaderablaufverfolgung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="64289-104">Callback to return the instructions generated from creating a shader trace.</span></span>

## <a name="members"></a><span data-ttu-id="64289-105">Member</span><span class="sxs-lookup"><span data-stu-id="64289-105">Members</span></span>

<span data-ttu-id="64289-106">Die **idebugshadercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64289-106">The **IDebugShaderCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="64289-107">**Idebugshadercallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64289-107">**IDebugShaderCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="64289-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="64289-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="64289-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="64289-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="64289-110">Die **idebugshadercallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="64289-110">The **IDebugShaderCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="64289-111">Methode</span><span class="sxs-lookup"><span data-stu-id="64289-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="64289-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64289-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="64289-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>Resultinstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="64289-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="64289-114">Ein Rückruf, der den Host über die Anmelde Informationen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64289-114">A callback that notifies the host of instructrion information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="64289-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64289-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="64289-116">Header</span><span class="sxs-lookup"><span data-stu-id="64289-116">Header</span></span></p></td><td><span data-ttu-id="64289-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="64289-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
