---
description: Die settimelineobject-Methode legt die Zeitachse fest, die von der Rendering-Engine verwendet wird.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'Unenderengine:: settimelineobject-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371242"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="f0bbc-103">Unenderengine:: settimelineobject-Methode</span><span class="sxs-lookup"><span data-stu-id="f0bbc-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="f0bbc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-104">\[Deprecated.</span></span> <span data-ttu-id="f0bbc-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f0bbc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0bbc-106">Die- `SetTimelineObject` Methode legt die Zeitachse fest, die das Rendermodul verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bbc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0bbc-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="f0bbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0bbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bbc-109">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="f0bbc-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="f0bbc-110">Zeiger auf die [**iamtimeline**](iamtimeline.md) -Schnittstelle des Timeline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bbc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0bbc-111">Return value</span></span>

<span data-ttu-id="f0bbc-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="f0bbc-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f0bbc-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0bbc-113">Return code</span></span>                                                                                            | <span data-ttu-id="f0bbc-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0bbc-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f0bbc-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f0bbc-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="f0bbc-117"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="f0bbc-118">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="f0bbc-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="f0bbc-120">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="f0bbc-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="f0bbc-122">Ungültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f0bbc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0bbc-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0bbc-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0bbc-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0bbc-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0bbc-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0bbc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0bbc-127">Requirements</span></span>



| <span data-ttu-id="f0bbc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0bbc-128">Requirement</span></span> | <span data-ttu-id="f0bbc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f0bbc-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bbc-130">Header</span><span class="sxs-lookup"><span data-stu-id="f0bbc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f0bbc-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0bbc-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0bbc-132">Library</span></span><br/> | <dl> <span data-ttu-id="f0bbc-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f0bbc-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0bbc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0bbc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bbc-135">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="f0bbc-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f0bbc-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f0bbc-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




