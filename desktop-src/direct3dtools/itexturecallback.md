---
description: Rückruf zum Schreiben einer Textur als DDS-Datei.
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Itexturecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 831de15656960cdc72ef2db50c1f3d13b8491e38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747369"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span data-ttu-id="0aa47-103"><span id="vspixengine.itexturecallback"></span>Itexturecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0aa47-103"><span id="vspixengine.itexturecallback"></span>ITextureCallback interface</span></span>

<span data-ttu-id="0aa47-104">Rückruf zum Schreiben einer Textur als DDS-Datei.</span><span class="sxs-lookup"><span data-stu-id="0aa47-104">Callback to write a texture as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="0aa47-105">Member</span><span class="sxs-lookup"><span data-stu-id="0aa47-105">Members</span></span>

<span data-ttu-id="0aa47-106">Die **itexturecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0aa47-106">The **ITextureCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0aa47-107">**Itexturecallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0aa47-107">**ITextureCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0aa47-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0aa47-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0aa47-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="0aa47-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0aa47-110">Die **itexturecallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0aa47-110">The **ITextureCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0aa47-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0aa47-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0aa47-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aa47-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0aa47-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0aa47-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0aa47-114">Ein Rückruf, der den Host über den benachrichtigt. Die DDS-Datei (DirectDraw Surface) mit Ergebnissen aus der zugeordneten Anforderung ist bereit.</span><span class="sxs-lookup"><span data-stu-id="0aa47-114">A callback that notifies the host that the .DDS (DirectDraw Surface) file containing results from the associated request are ready.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0aa47-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aa47-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0aa47-116">Header</span><span class="sxs-lookup"><span data-stu-id="0aa47-116">Header</span></span></p></td><td><span data-ttu-id="0aa47-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0aa47-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
