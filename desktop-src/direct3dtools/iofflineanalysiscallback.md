---
description: Rückruf für gibt Offline Analysedaten zurück.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iofflineanalysiscallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 496ca07544cdc38ff9f0e3f29c0ebbd2b9e8753c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340095"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span data-ttu-id="0d93f-103"><span id="vspixengine.iofflineanalysiscallback"></span>Iofflineanalysiscallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0d93f-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback interface</span></span>

<span data-ttu-id="0d93f-104">Rückruf für gibt Offline Analysedaten zurück.</span><span class="sxs-lookup"><span data-stu-id="0d93f-104">Callback to returns offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="0d93f-105">Member</span><span class="sxs-lookup"><span data-stu-id="0d93f-105">Members</span></span>

<span data-ttu-id="0d93f-106">Die **iofflineanalysiscallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d93f-106">The **IOfflineAnalysisCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0d93f-107">**Iofflineanalysiscallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0d93f-107">**IOfflineAnalysisCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0d93f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0d93f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0d93f-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="0d93f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0d93f-110">Die **iofflineanalysiscallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0d93f-110">The **IOfflineAnalysisCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0d93f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0d93f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0d93f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d93f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0d93f-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>Offlineanalysiscomplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d93f-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0d93f-114">Eine Rückruffunktion, mit der der Host benachrichtigt wird, dass die Offline Analyse abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0d93f-114">A callback function used to notify the host that offline analysis has completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="0d93f-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>Offlineanalysisprogress</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d93f-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0d93f-116">Eine Rückruffunktion, die verwendet wird, um den Host den Status der Offline Analyse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0d93f-116">A callback function used to notify the host of offline analysis progress.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0d93f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d93f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0d93f-118">Header</span><span class="sxs-lookup"><span data-stu-id="0d93f-118">Header</span></span></p></td><td><span data-ttu-id="0d93f-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0d93f-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
