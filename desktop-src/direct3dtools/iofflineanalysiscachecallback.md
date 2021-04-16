---
description: Rückruf, der Informationen darüber zurückgibt, ob eine Offline Anforderung zwischengespeichert wird.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iofflineanalysiscachecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E226B1A6-D028-4562-9C8C-D25EC91A2DB2
api_name:
- IOfflineAnalysisCacheCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e0107f97353bf7ad5b62472bc54a2b8388fb6aff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522368"
---
# <a name="span-idvspixengineiofflineanalysiscachecallbackspaniofflineanalysiscachecallback-interface"></a><span data-ttu-id="e034f-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>Iofflineanalysiscachecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e034f-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback interface</span></span>

<span data-ttu-id="e034f-104">Rückruf, der Informationen darüber zurückgibt, ob eine Offline Anforderung zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e034f-104">Callback to return information on whether an offline request is cached or not.</span></span>

## <a name="members"></a><span data-ttu-id="e034f-105">Member</span><span class="sxs-lookup"><span data-stu-id="e034f-105">Members</span></span>

<span data-ttu-id="e034f-106">Die **iofflineanalysiscachecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e034f-106">The **IOfflineAnalysisCacheCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e034f-107">**Iofflineanalysiscachecallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e034f-107">**IOfflineAnalysisCacheCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e034f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e034f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e034f-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="e034f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e034f-110">Die **iofflineanalysiscachecallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e034f-110">The **IOfflineAnalysisCacheCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e034f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e034f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e034f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e034f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e034f-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>Offlineanalaysisreportavailabilitycallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e034f-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e034f-114">Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, welche Frames Offline Analyseberichte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e034f-114">A callback function used to notify the host about which frames have offline analysis reports available.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e034f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e034f-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e034f-116">Header</span><span class="sxs-lookup"><span data-stu-id="e034f-116">Header</span></span></p></td><td><span data-ttu-id="e034f-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e034f-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
