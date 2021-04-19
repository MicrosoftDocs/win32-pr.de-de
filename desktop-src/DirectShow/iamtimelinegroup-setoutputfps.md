---
description: Die setoutputfps-Methode legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Iamtimelinegroup:: setoutputfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373939"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="4e44a-103">Iamtimelinegroup:: setoutputfps-Methode</span><span class="sxs-lookup"><span data-stu-id="4e44a-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="4e44a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4e44a-104">\[Deprecated.</span></span> <span data-ttu-id="4e44a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4e44a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4e44a-106">Die- `SetOutputFPS` Methode legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="4e44a-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e44a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e44a-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="4e44a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e44a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e44a-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="4e44a-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="4e44a-110">Ausgabe Frame Rate für diese Gruppe in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4e44a-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="4e44a-111">Der Wert kann nicht gleich 0 (null) sein und darf nicht mehr als sieben Ziffern nach der Dezimalstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="4e44a-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e44a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e44a-112">Return value</span></span>

<span data-ttu-id="4e44a-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e44a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e44a-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e44a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e44a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e44a-115">Remarks</span></span>

<span data-ttu-id="4e44a-116">Die gerenderte Ausgabe dieser Gruppe wird mit der angegebenen Framerate ausgeführt, und alle bearbeitvorgänge im Quellmaterial werden wie durch die Frame Rate definiert auf die nächste Frame Grenze gerundet.</span><span class="sxs-lookup"><span data-stu-id="4e44a-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="4e44a-117">Verwenden Sie für eine optimale Leistung die gleiche Framerate für alle Gruppen, Videos und Audiodateien.</span><span class="sxs-lookup"><span data-stu-id="4e44a-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="4e44a-118">Die [**iamtimelinegroup::**](iamtimelinegroup-setsmartrecompressformat.md) -Methode zum Festlegen der Methode überschreibt die Framerate.</span><span class="sxs-lookup"><span data-stu-id="4e44a-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="4e44a-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4e44a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4e44a-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4e44a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4e44a-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4e44a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4e44a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e44a-122">Requirements</span></span>



| <span data-ttu-id="4e44a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e44a-123">Requirement</span></span> | <span data-ttu-id="4e44a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4e44a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e44a-125">Header</span><span class="sxs-lookup"><span data-stu-id="4e44a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4e44a-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4e44a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4e44a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e44a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4e44a-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4e44a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e44a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e44a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e44a-130">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4e44a-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="4e44a-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="4e44a-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




