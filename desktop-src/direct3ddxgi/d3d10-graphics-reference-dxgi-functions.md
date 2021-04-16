---
description: Dieser Abschnitt enthält Informationen zu den Funktionen, die von DXGI bereitgestellt werden.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520875"
---
# <a name="dxgi-functions"></a><span data-ttu-id="ede90-103">DXGI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ede90-103">DXGI Functions</span></span>

<span data-ttu-id="ede90-104">Dieser Abschnitt enthält Informationen zu den Funktionen, die von DXGI bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ede90-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ede90-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ede90-105">In this section</span></span>



| <span data-ttu-id="ede90-106">Thema</span><span class="sxs-lookup"><span data-stu-id="ede90-106">Topic</span></span>                                                                                   | <span data-ttu-id="ede90-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ede90-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ede90-108">**"Kreatedxgifactory"**</span><span class="sxs-lookup"><span data-stu-id="ede90-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="ede90-109">Erstellt eine DXGI 1,0-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ede90-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="ede90-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="ede90-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="ede90-111">Erstellt eine DXGI 1,1-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ede90-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="ede90-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="ede90-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="ede90-113">Erstellt eine DXGI 1,3-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ede90-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="ede90-114">In Windows 8 würde jede DXGI-Factory, die erstellt wurde, während DXGIDebug.dll im System vorhanden war, Sie laden und verwenden.</span><span class="sxs-lookup"><span data-stu-id="ede90-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="ede90-115">Ab Windows 8.1 fordern apps explizit an, dass Sie stattdessen laden DXGIDebug.dll.</span><span class="sxs-lookup"><span data-stu-id="ede90-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="ede90-116">Verwenden Sie [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) , und geben Sie das DXGI- \_ \_ \_ Debugflag Create Factory an, um DXGIDebug.dll anzufordern. die dll wird geladen, wenn Sie auf dem System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ede90-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="ede90-117">**Dxgideclareadapterremovalsupport**</span><span class="sxs-lookup"><span data-stu-id="ede90-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="ede90-118">Ermöglicht einem Prozess, anzugeben, dass er für alle zu entfernenden Grafikgeräte robust ist.</span><span class="sxs-lookup"><span data-stu-id="ede90-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="ede90-119">**Dxgigetdebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ede90-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="ede90-120">Ruft eine Debugschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="ede90-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ede90-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="ede90-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="ede90-122">Ruft eine Schnittstelle ab, die Windows Store-Apps zum Debuggen der Microsoft DirectX Graphics Infrastructure (DXGI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ede90-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ede90-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ede90-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede90-124">DXGI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ede90-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




