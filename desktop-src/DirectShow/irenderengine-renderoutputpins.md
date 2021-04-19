---
description: Die renderoutputpins-Methode erstellt den Teil der Vorschau des Filter Diagramms.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Unenderengine:: renderoutputpins-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373896"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="9ced4-103">Unenderengine:: renderoutputpins-Methode</span><span class="sxs-lookup"><span data-stu-id="9ced4-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="9ced4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9ced4-104">\[Deprecated.</span></span> <span data-ttu-id="9ced4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9ced4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ced4-106">Die- `RenderOutputPins` Methode erstellt den Teil der Vorschau des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="9ced4-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ced4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ced4-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="9ced4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ced4-108">Parameters</span></span>

<span data-ttu-id="9ced4-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ced4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ced4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ced4-110">Return value</span></span>

<span data-ttu-id="9ced4-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ced4-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="9ced4-112">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9ced4-112">The following are possible values:</span></span>



| <span data-ttu-id="9ced4-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ced4-113">Return code</span></span>                                                                                                  | <span data-ttu-id="9ced4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ced4-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ced4-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="9ced4-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9ced4-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9ced4-117"><dt>**VFW \_ S \_ -Audiodatei \_ nicht \_ gerendert**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="9ced4-118">Der Audiostream kann nicht wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ced4-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="9ced4-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="9ced4-120">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="9ced4-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="9ced4-121"><dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="9ced4-122">Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="9ced4-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9ced4-123"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="9ced4-124">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ced4-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="9ced4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ced4-125">Remarks</span></span>

<span data-ttu-id="9ced4-126">Rufen Sie vor dem Aufrufen dieser Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " auf, um das Front-End des Diagramms zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ced4-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="9ced4-127">Um einen anderen Vorgang als die Vorschau auszuführen, dürfen Sie diese Methode nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9ced4-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="9ced4-128">Rufen Sie stattdessen " [**irienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " auf, um Zeiger auf die Ausgabe Pins zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ced4-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="9ced4-129">Wenn auf dem Computer des Benutzers keine Soundkarte vorhanden ist, gibt diese Methode VFW \_ s \_ -Audiodaten zurück, die \_ nicht \_ gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="9ced4-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="9ced4-130">In diesem Fall wird keine Audiovorschau angezeigt, aber die Video Vorschau ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="9ced4-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="9ced4-131">Wenn die PIN aus einer Videogruppe besteht, erstellt diese Methode ein Videofenster.</span><span class="sxs-lookup"><span data-stu-id="9ced4-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="9ced4-132">Der aufrufenden Thread muss Nachrichten verteilen – beispielsweise, um das Fenster zu verschieben oder auf Mausklicks im Client Bereich des Fensters zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="9ced4-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="9ced4-133">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9ced4-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ced4-134">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9ced4-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ced4-135">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ced4-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ced4-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ced4-136">Requirements</span></span>



| <span data-ttu-id="9ced4-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ced4-137">Requirement</span></span> | <span data-ttu-id="9ced4-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9ced4-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ced4-139">Header</span><span class="sxs-lookup"><span data-stu-id="9ced4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="9ced4-140"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ced4-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ced4-141">Library</span></span><br/> | <dl> <span data-ttu-id="9ced4-142"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9ced4-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ced4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ced4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ced4-144">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="9ced4-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="9ced4-145">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="9ced4-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




