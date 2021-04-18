---
description: Die getgroupoutputpin-Methode ruft die Ausgabe-PIN für die angegebene Gruppe ab.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Unenderengine:: getgroupoutputpin-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365540"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="238db-103">Unenderengine:: getgroupoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="238db-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="238db-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="238db-104">\[Deprecated.</span></span> <span data-ttu-id="238db-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="238db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="238db-106">Die- `GetGroupOutputPin` Methode ruft die Ausgabepin für die angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="238db-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="238db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="238db-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="238db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="238db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238db-109">*Gruppieren*</span><span class="sxs-lookup"><span data-stu-id="238db-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="238db-110">NULL basierter Index, der die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="238db-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="238db-111">*pprenderpin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="238db-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="238db-112">Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="238db-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="238db-113">Return value</span></span>

<span data-ttu-id="238db-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="238db-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="238db-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="238db-115">Possible values include the following:</span></span>



| <span data-ttu-id="238db-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="238db-116">Return code</span></span>                                                                                                  | <span data-ttu-id="238db-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="238db-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="238db-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="238db-119">Die Gruppe verfügt über keine Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="238db-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="238db-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="238db-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="238db-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="238db-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="238db-123">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="238db-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="238db-124"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="238db-125">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="238db-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="238db-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="238db-127">Ungültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="238db-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="238db-128"><dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="238db-129">Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="238db-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="238db-130"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="238db-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="238db-131">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="238db-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="238db-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="238db-132">Remarks</span></span>

<span data-ttu-id="238db-133">Rufen Sie vor dem Aufrufen dieser Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " auf, um das Front-End des Diagramms zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="238db-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="238db-134">Jede Gruppe stellt einen einzelnen Mediendaten Strom dar, und das Front-End verfügt über eine entsprechende Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="238db-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="238db-135">Mit dieser Methode können Sie den renderingteil eines Datei Schreib Diagramms erstellen.</span><span class="sxs-lookup"><span data-stu-id="238db-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="238db-136">Verbinden Sie die Ausgabe Pins mit Multiplexer-Filtern und dateiwriter-filtern.</span><span class="sxs-lookup"><span data-stu-id="238db-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="238db-137">Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="238db-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="238db-138">In der Vorschauversion müssen Sie diese Methode nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="238db-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="238db-139">Nennen Sie einfach **connectfrontend** , gefolgt von " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md)".</span><span class="sxs-lookup"><span data-stu-id="238db-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="238db-140">Wenn die Methode S OK zurückgibt \_ , hat die zurückgegebene **IPin** -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="238db-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="238db-141">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="238db-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="238db-142">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="238db-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="238db-143">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="238db-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="238db-144">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="238db-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="238db-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="238db-145">Requirements</span></span>



| <span data-ttu-id="238db-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="238db-146">Requirement</span></span> | <span data-ttu-id="238db-147">Wert</span><span class="sxs-lookup"><span data-stu-id="238db-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="238db-148">Header</span><span class="sxs-lookup"><span data-stu-id="238db-148">Header</span></span><br/>  | <dl> <span data-ttu-id="238db-149"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="238db-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="238db-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="238db-150">Library</span></span><br/> | <dl> <span data-ttu-id="238db-151"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="238db-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="238db-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="238db-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238db-153">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="238db-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="238db-154">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="238db-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




