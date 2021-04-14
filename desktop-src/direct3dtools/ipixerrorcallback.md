---
description: Rückruf von Engine zum Behandeln von Fehlern.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixerrorcallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392470"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="7bf02-103"><span id="vspixengine.ipixerrorcallback"></span>Ipixerrorcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7bf02-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="7bf02-104">Rückruf von Engine zum Behandeln von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="7bf02-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="7bf02-105">Member</span><span class="sxs-lookup"><span data-stu-id="7bf02-105">Members</span></span>

<span data-ttu-id="7bf02-106">Die **ipixerrorcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7bf02-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7bf02-107">**Ipixerrorcallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7bf02-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="7bf02-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="7bf02-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="7bf02-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="7bf02-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="7bf02-110">Die **ipixerrorcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7bf02-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="7bf02-111">Methode</span><span class="sxs-lookup"><span data-stu-id="7bf02-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="7bf02-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bf02-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="7bf02-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>Errorlistcallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7bf02-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7bf02-114">Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7bf02-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="7bf02-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>Messagescallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7bf02-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7bf02-116">Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7bf02-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="7bf02-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>Warninglistcallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7bf02-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7bf02-118">Ein Rückruf, der den Host über Warnungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7bf02-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="7bf02-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bf02-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7bf02-120">Header</span><span class="sxs-lookup"><span data-stu-id="7bf02-120">Header</span></span></p></td><td><span data-ttu-id="7bf02-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7bf02-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
