---
description: Anforderung für Offline Analysedaten.
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iofflineanalysisrequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 980c4d9f3b745d197789e5e450e0bf782127ca0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860401"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span data-ttu-id="dd9f0-103"><span id="vspixengine.iofflineanalysisrequest"></span>Iofflineanalysisrequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dd9f0-103"><span id="vspixengine.iofflineanalysisrequest"></span>IOfflineAnalysisRequest interface</span></span>

<span data-ttu-id="dd9f0-104">Anforderung für Offline Analysedaten.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-104">Request for offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="dd9f0-105">Member</span><span class="sxs-lookup"><span data-stu-id="dd9f0-105">Members</span></span>

<span data-ttu-id="dd9f0-106">Die **iofflineanalysisrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-106">The **IOfflineAnalysisRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd9f0-107">**Iofflineanalysisrequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd9f0-107">**IOfflineAnalysisRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="dd9f0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd9f0-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="dd9f0-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="dd9f0-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="dd9f0-110">Die **iofflineanalysisrequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-110">The **IOfflineAnalysisRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="dd9f0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="dd9f0-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="dd9f0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd9f0-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="dd9f0-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>Cancelofflineanalysisasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f0-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="dd9f0-114">Anforderungen zum Abbrechen der Offline Analyse in einer Offline Analyse Anforderung.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-114">Requests to cancel offline analysis in an offline analysis request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="dd9f0-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>Requestofflineanalysisasync</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd9f0-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="dd9f0-116">Fordert an, eine Offline Analyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-116">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="dd9f0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd9f0-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dd9f0-118">Header</span><span class="sxs-lookup"><span data-stu-id="dd9f0-118">Header</span></span></p></td><td><span data-ttu-id="dd9f0-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="dd9f0-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
