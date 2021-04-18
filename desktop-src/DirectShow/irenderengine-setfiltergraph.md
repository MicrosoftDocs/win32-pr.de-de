---
description: Die setfiltergraph-Methode gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Unenderengine:: setfiltergraph-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371564"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="b8892-103">Unenderengine:: setfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="b8892-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="b8892-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b8892-104">\[Deprecated.</span></span> <span data-ttu-id="b8892-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b8892-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8892-106">Die- `SetFilterGraph` Methode gibt ein Filter Diagramm für die zu verwendende Rendering-Engine an.</span><span class="sxs-lookup"><span data-stu-id="b8892-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8892-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8892-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="b8892-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8892-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8892-109">*PFG*</span><span class="sxs-lookup"><span data-stu-id="b8892-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="b8892-110">Ein Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="b8892-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8892-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8892-111">Return value</span></span>

<span data-ttu-id="b8892-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="b8892-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b8892-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b8892-113">Return code</span></span>                                                                                            | <span data-ttu-id="b8892-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8892-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b8892-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8892-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b8892-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b8892-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="b8892-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b8892-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="b8892-118">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="b8892-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="b8892-119"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="b8892-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="b8892-120">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="b8892-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8892-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8892-121">Remarks</span></span>

<span data-ttu-id="b8892-122">Die meisten Anwendungen müssen diese Methode nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b8892-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="b8892-123">Es ist eher typisch, dass die Renderingengine das Diagramm für Sie erstellt, indem Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b8892-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="b8892-124">Diese Methode schlägt fehl, wenn die Renderingengine bereits über ein Filter Diagramm verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8892-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="b8892-125">Rufen Sie niemals einen Zeiger auf ein Filter Diagramm ab, das von einem Rendermodul erstellt wurde, und verwenden Sie es dann als Parameter für diese Methode in einer anderen Renderingengine.</span><span class="sxs-lookup"><span data-stu-id="b8892-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="b8892-126">Dies führt zu unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="b8892-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="b8892-127">Die **connectfrontend** -Methode führt ein beliebiges vorhandenes Filter Diagramm aus, behält aber dieselbe Filter-Graph-Manager-Instanz bei.</span><span class="sxs-lookup"><span data-stu-id="b8892-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="b8892-128">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b8892-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8892-129">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b8892-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8892-130">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8892-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8892-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8892-131">Requirements</span></span>



| <span data-ttu-id="b8892-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8892-132">Requirement</span></span> | <span data-ttu-id="b8892-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b8892-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8892-134">Header</span><span class="sxs-lookup"><span data-stu-id="b8892-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b8892-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b8892-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8892-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8892-136">Library</span></span><br/> | <dl> <span data-ttu-id="b8892-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b8892-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8892-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8892-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8892-139">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="b8892-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="b8892-140">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b8892-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




