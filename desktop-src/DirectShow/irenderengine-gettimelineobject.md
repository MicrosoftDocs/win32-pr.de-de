---
description: Die gettimelineobject-Methode ruft die Zeitachse ab, die von der Rendering-Engine zurzeit verwendet wird.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Unenderengine:: gettimelineobject-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366807"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="39ecd-103">Unenderengine:: gettimelineobject-Methode</span><span class="sxs-lookup"><span data-stu-id="39ecd-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="39ecd-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="39ecd-104">\[Deprecated.</span></span> <span data-ttu-id="39ecd-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="39ecd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="39ecd-106">Die- `GetTimelineObject` Methode ruft die Zeitachse ab, die die Renderingengine zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="39ecd-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ecd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39ecd-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="39ecd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ecd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ecd-109">*pptimeline* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39ecd-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39ecd-110">Empfängt einen Zeiger auf die [**iamtimeline**](iamtimeline.md) -Schnittstelle der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="39ecd-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="39ecd-111">Wenn keine Zeitachse vorhanden ist, erhält Sie den Wert **null** .</span><span class="sxs-lookup"><span data-stu-id="39ecd-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ecd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39ecd-112">Return value</span></span>

<span data-ttu-id="39ecd-113">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="39ecd-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="39ecd-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="39ecd-114">Return code</span></span>                                                                                            | <span data-ttu-id="39ecd-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39ecd-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="39ecd-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="39ecd-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="39ecd-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="39ecd-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="39ecd-119">Ungültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="39ecd-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="39ecd-120"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="39ecd-121">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="39ecd-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39ecd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39ecd-122">Remarks</span></span>

<span data-ttu-id="39ecd-123">Wenn bei der Rückgabe der Wert von *\* pptimeline* ungleich **null** ist, weist die **iamtimeline** -Schnittstelle eine ausstehende Verweis Anzahl auf.</span><span class="sxs-lookup"><span data-stu-id="39ecd-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="39ecd-124">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="39ecd-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="39ecd-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="39ecd-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="39ecd-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="39ecd-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="39ecd-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39ecd-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39ecd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39ecd-128">Requirements</span></span>



| <span data-ttu-id="39ecd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39ecd-129">Requirement</span></span> | <span data-ttu-id="39ecd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="39ecd-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39ecd-131">Header</span><span class="sxs-lookup"><span data-stu-id="39ecd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="39ecd-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="39ecd-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39ecd-133">Library</span></span><br/> | <dl> <span data-ttu-id="39ecd-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="39ecd-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ecd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39ecd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ecd-136">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="39ecd-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="39ecd-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="39ecd-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




