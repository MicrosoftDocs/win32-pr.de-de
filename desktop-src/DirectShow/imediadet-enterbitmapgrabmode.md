---
description: Die enterbitmapgrabmode-Methode schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem angegebenen Zeitpunkt.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Imediadet:: enterbitmapgrabmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359382"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="5e5de-103">Imediadet:: enterbitmapgrabmode-Methode</span><span class="sxs-lookup"><span data-stu-id="5e5de-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="5e5de-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5e5de-104">\[Deprecated.</span></span> <span data-ttu-id="5e5de-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5e5de-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5e5de-106">Die `EnterBitmapGrabMode` -Methode schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="5e5de-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e5de-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="5e5de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e5de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5de-109">*Streamtime*</span><span class="sxs-lookup"><span data-stu-id="5e5de-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5e5de-110">Die Zeit (in Sekunden), die das Diagramm sucht.</span><span class="sxs-lookup"><span data-stu-id="5e5de-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5de-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e5de-111">Return value</span></span>

<span data-ttu-id="5e5de-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e5de-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5e5de-113">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="5e5de-113">Possible values include the following:</span></span>



| <span data-ttu-id="5e5de-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5e5de-114">Return code</span></span>                                                                                             | <span data-ttu-id="5e5de-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e5de-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="5e5de-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="5e5de-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5e5de-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5e5de-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="5e5de-119">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="5e5de-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="5e5de-120"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="5e5de-121">Die Quelldatei enthält keinen Videostream.</span><span class="sxs-lookup"><span data-stu-id="5e5de-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="5e5de-122"><dt>**VFW \_ E \_ Zeit \_ abgelaufen**</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="5e5de-123">Timeout beim Suchbefehl.</span><span class="sxs-lookup"><span data-stu-id="5e5de-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="5e5de-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e5de-124">Remarks</span></span>

<span data-ttu-id="5e5de-125">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="5e5de-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="5e5de-126">Mit dieser Methode wird der [**Sample Grabber**](sample-grabber-filter.md) Filter in das Filter Diagramm eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5e5de-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="5e5de-127">Sie können dann [**imediadet:: getsamplegrabber**](imediadet-getsamplegrabber.md) aufrufen, um einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e5de-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="5e5de-128">Sobald der Medien Detektor in den bitmapingmodus wechselt, funktionieren die verschiedenen Informationsmethoden in **imediadet** nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="5e5de-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="5e5de-129">Mit der [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode oder der [**imediadet:: Write-Bitmapbits**](imediadet-writebitmapbits.md) -Methode wird der Medien Detektor auch in den bitmapmodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="5e5de-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="5e5de-130">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5e5de-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5e5de-131">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5e5de-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5e5de-132">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e5de-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e5de-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e5de-133">Requirements</span></span>



| <span data-ttu-id="5e5de-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e5de-134">Requirement</span></span> | <span data-ttu-id="5e5de-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5e5de-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5de-136">Header</span><span class="sxs-lookup"><span data-stu-id="5e5de-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5e5de-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5e5de-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e5de-138">Library</span></span><br/> | <dl> <span data-ttu-id="5e5de-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5e5de-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5de-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e5de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5de-141">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5e5de-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="5e5de-142">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5e5de-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




