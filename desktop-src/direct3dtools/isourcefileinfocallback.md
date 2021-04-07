---
description: Rückruf, der Quelldatei Informationen von einer Aufruf Liste zurückgibt.
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Isourcefileingefocallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747584"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="f3bd1-103"><span id="vspixengine.isourcefileinfocallback"></span>Isourcefileingefocallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f3bd1-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="f3bd1-104">Rückruf, der Quelldatei Informationen von einer Aufruf Liste zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="f3bd1-105">Member</span><span class="sxs-lookup"><span data-stu-id="f3bd1-105">Members</span></span>

<span data-ttu-id="f3bd1-106">Die **isourcefileingefocallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3bd1-107">**Isourcefileinfocallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f3bd1-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f3bd1-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f3bd1-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="f3bd1-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f3bd1-110">Die **isourcefileingefocallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f3bd1-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f3bd1-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f3bd1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3bd1-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f3bd1-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3bd1-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f3bd1-114">Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Quelldateien zu benachrichtigen, die der Aufruf Liste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f3bd1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3bd1-116">Header</span><span class="sxs-lookup"><span data-stu-id="f3bd1-116">Header</span></span></p></td><td><span data-ttu-id="f3bd1-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f3bd1-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
