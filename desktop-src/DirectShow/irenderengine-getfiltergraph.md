---
description: Die getfiltergraph-Methode ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Unenderengine:: getfiltergraph-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356310"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="207ac-103">Unenderengine:: getfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="207ac-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="207ac-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="207ac-104">\[Deprecated.</span></span> <span data-ttu-id="207ac-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="207ac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="207ac-106">Die- `GetFilterGraph` Methode ruft das Filter Diagramm ab, das von der Rendering-Engine erstellt wurde (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="207ac-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="207ac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="207ac-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="207ac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="207ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207ac-109">*ppfg* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="207ac-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="207ac-110">Empfängt einen Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="207ac-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="207ac-111">Er empfängt den Wert **null** , wenn kein Filter Diagramm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="207ac-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207ac-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="207ac-112">Return value</span></span>

<span data-ttu-id="207ac-113">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="207ac-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="207ac-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="207ac-114">Return code</span></span>                                                                                            | <span data-ttu-id="207ac-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="207ac-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="207ac-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="207ac-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="207ac-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="207ac-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="207ac-118"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="207ac-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="207ac-119">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="207ac-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="207ac-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="207ac-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="207ac-121">Ungültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="207ac-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="207ac-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="207ac-122">Remarks</span></span>

<span data-ttu-id="207ac-123">Verwenden Sie die Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) ", um das Front-End des Filter Diagramms zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="207ac-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="207ac-124">Verwenden Sie für die Vorschauversion den " [**unenderengine:: renderoutputpins**](irenderengine-renderoutputpins.md) ", um das Diagramm abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="207ac-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="207ac-125">Für die Dateiausgabe verbinden Sie das Front-End mit einer Kombination aus MUX/dateiwriter.</span><span class="sxs-lookup"><span data-stu-id="207ac-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="207ac-126">Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="207ac-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="207ac-127">Das resultierende Diagramm kann ausgeführt, angehalten, beendet und Seeding ausgeführt werden. die Wiedergabe Rate kann jedoch nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="207ac-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="207ac-128">Wenn der Wert von *\* ppfg* bei Rückgabe ungleich **null** ist, weist die **igraphbuilder** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="207ac-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="207ac-129">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="207ac-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="207ac-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="207ac-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="207ac-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="207ac-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="207ac-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="207ac-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="207ac-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="207ac-133">Requirements</span></span>



| <span data-ttu-id="207ac-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="207ac-134">Requirement</span></span> | <span data-ttu-id="207ac-135">Wert</span><span class="sxs-lookup"><span data-stu-id="207ac-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="207ac-136">Header</span><span class="sxs-lookup"><span data-stu-id="207ac-136">Header</span></span><br/>  | <dl> <span data-ttu-id="207ac-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="207ac-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="207ac-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="207ac-138">Library</span></span><br/> | <dl> <span data-ttu-id="207ac-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="207ac-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207ac-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="207ac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207ac-141">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="207ac-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="207ac-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="207ac-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




