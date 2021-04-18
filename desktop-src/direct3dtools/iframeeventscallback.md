---
description: Rückruf, um die Liste der Ereignisse in einem Frame zurückzugeben.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iframeeventscallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344783"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="d282a-103"><span id="vspixengine.iframeeventscallback"></span>Iframeeventscallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d282a-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="d282a-104">Rückruf, um die Liste der Ereignisse in einem Frame zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d282a-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="d282a-105">Member</span><span class="sxs-lookup"><span data-stu-id="d282a-105">Members</span></span>

<span data-ttu-id="d282a-106">Die **iframeeventscallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d282a-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d282a-107">**Iframeeventscallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d282a-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d282a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d282a-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d282a-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="d282a-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d282a-110">Die **iframeeventscallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d282a-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d282a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d282a-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d282a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d282a-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d282a-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>Getsupportedebug Columns</strong></a></span><span class="sxs-lookup"><span data-stu-id="d282a-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d282a-114">Ruft Informationen darüber ab, welche Spalten (Ereignisdaten Typen) von der Ereignisliste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d282a-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d282a-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="d282a-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d282a-116">Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Ereignisse in der Ereignisliste zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="d282a-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d282a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d282a-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d282a-118">Header</span><span class="sxs-lookup"><span data-stu-id="d282a-118">Header</span></span></p></td><td><span data-ttu-id="d282a-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d282a-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
