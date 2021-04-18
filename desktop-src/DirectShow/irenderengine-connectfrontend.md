---
description: Die connectfrontend-Methode erstellt das Front-End des Filter Diagramms aus der aktuellen Zeitachse.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Unenderengine:: connectfrontend-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371225"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="cddbe-103">Unenderengine:: connectfrontend-Methode</span><span class="sxs-lookup"><span data-stu-id="cddbe-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="cddbe-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cddbe-104">\[Deprecated.</span></span> <span data-ttu-id="cddbe-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cddbe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cddbe-106">Mit der- `ConnectFrontEnd` Methode wird das Front-End des Filter Diagramms aus der aktuellen Zeitachse erstellt.</span><span class="sxs-lookup"><span data-stu-id="cddbe-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddbe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cddbe-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="cddbe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cddbe-108">Parameters</span></span>

<span data-ttu-id="cddbe-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cddbe-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cddbe-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cddbe-110">Return value</span></span>

<span data-ttu-id="cddbe-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cddbe-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cddbe-112">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="cddbe-112">Possible return values include the following:</span></span>



| <span data-ttu-id="cddbe-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cddbe-113">Return code</span></span>                                                                                                  | <span data-ttu-id="cddbe-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cddbe-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cddbe-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="cddbe-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cddbe-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="cddbe-117"><dt>**S \_ Warnung \_ outputreset**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="cddbe-118">Der Renderingbereich des Diagramms wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cddbe-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="cddbe-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="cddbe-120">Es wurde keine Zeitachse für diese Renderingengine</span><span class="sxs-lookup"><span data-stu-id="cddbe-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="cddbe-121"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="cddbe-122">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="cddbe-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cddbe-123"><dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="cddbe-124">Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="cddbe-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cddbe-125"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="cddbe-126">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cddbe-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="cddbe-127"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="cddbe-128">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="cddbe-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="cddbe-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cddbe-129">Remarks</span></span>

<span data-ttu-id="cddbe-130">Diese Methode erstellt nicht den renderingteil des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="cddbe-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="cddbe-131">Die Anwendung muss die Ausgabe Pins auf dem Front-End mit den gewünschten renderingfiltern verbinden:</span><span class="sxs-lookup"><span data-stu-id="cddbe-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="cddbe-132">Um die Vorschau anzuzeigen, wenden Sie die Methode " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md) " an.</span><span class="sxs-lookup"><span data-stu-id="cddbe-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="cddbe-133">Um eine Datei auszugeben, rufen Sie die Datei " [**faienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " auf, um die Ausgabe-PIN für jede Gruppe abzurufen, und verbinden Sie dann die Pins mit einem Multiplexer-Filter.</span><span class="sxs-lookup"><span data-stu-id="cddbe-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="cddbe-134">Wenn Sie die einfache Renderingengine verwenden, erzeugen die Ausgabe Pins auf dem Front-End unkomprimierte Daten.</span><span class="sxs-lookup"><span data-stu-id="cddbe-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="cddbe-135">Wenn Sie die Smart-Rendering-Engine verwenden, erzeugen die Ausgabe Pins komprimierte Daten.</span><span class="sxs-lookup"><span data-stu-id="cddbe-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="cddbe-136">Wenn Sie die Zeitachse nach dem Erstellen des Filter Diagramms ändern, müssen Sie erneut einen Aufruf `ConnectFrontEnd` zum erneuten Erstellen des Front-Ends durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="cddbe-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="cddbe-137">Die-Methode behält den Renderingbereich des Diagramms bei, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="cddbe-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="cddbe-138">Wenn Sie jedoch eine Gruppe hinzufügen oder löschen oder die Reihenfolge der Gruppen ändern, `ConnectFrontEnd` Löscht den renderingteil, und die Anwendung muss Sie neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cddbe-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="cddbe-139">Wenn die-Methode den renderingteil löscht, gibt Sie "S \_ Warn \_ outputreset" zurück.</span><span class="sxs-lookup"><span data-stu-id="cddbe-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="cddbe-140">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cddbe-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cddbe-141">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cddbe-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cddbe-142">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cddbe-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cddbe-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cddbe-143">Requirements</span></span>



| <span data-ttu-id="cddbe-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cddbe-144">Requirement</span></span> | <span data-ttu-id="cddbe-145">Wert</span><span class="sxs-lookup"><span data-stu-id="cddbe-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cddbe-146">Header</span><span class="sxs-lookup"><span data-stu-id="cddbe-146">Header</span></span><br/>  | <dl> <span data-ttu-id="cddbe-147"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cddbe-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cddbe-148">Library</span></span><br/> | <dl> <span data-ttu-id="cddbe-149"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cddbe-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cddbe-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cddbe-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddbe-151">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="cddbe-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="cddbe-152">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cddbe-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




