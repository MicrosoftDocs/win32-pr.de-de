---
description: Die get \_ Framerate-Methode ruft die Framerate des aktuellen Streams ab. Der Stream muss ein Videostream sein.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Imediadet:: get_FrameRate-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362060"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="3c758-104">Imediadet:: get \_ Framerate-Methode</span><span class="sxs-lookup"><span data-stu-id="3c758-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="3c758-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3c758-105">\[Deprecated.</span></span> <span data-ttu-id="3c758-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3c758-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c758-107">Die- `get_FrameRate` Methode ruft die Framerate des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="3c758-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="3c758-108">Der Stream muss ein Videostream sein.</span><span class="sxs-lookup"><span data-stu-id="3c758-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c758-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c758-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3c758-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c758-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c758-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3c758-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3c758-112">Empfängt die Framerate in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3c758-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c758-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c758-113">Return value</span></span>

<span data-ttu-id="3c758-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3c758-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3c758-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="3c758-115">Possible values include the following:</span></span>



| <span data-ttu-id="3c758-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3c758-116">Return code</span></span>                                                                                             | <span data-ttu-id="3c758-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c758-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="3c758-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="3c758-119">Der Video Format Header gibt keine Frame Rate an.</span><span class="sxs-lookup"><span data-stu-id="3c758-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="3c758-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="3c758-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3c758-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="3c758-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="3c758-123">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="3c758-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="3c758-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="3c758-125">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="3c758-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="3c758-126"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="3c758-127">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="3c758-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="3c758-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c758-128">Remarks</span></span>

<span data-ttu-id="3c758-129">Diese Methode kann die Framerate nicht aus einer ASF-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="3c758-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="3c758-130">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="3c758-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="3c758-131">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="3c758-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="3c758-132">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="3c758-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c758-133">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3c758-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c758-134">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3c758-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c758-135">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c758-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c758-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c758-136">Requirements</span></span>



| <span data-ttu-id="3c758-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c758-137">Requirement</span></span> | <span data-ttu-id="3c758-138">Wert</span><span class="sxs-lookup"><span data-stu-id="3c758-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c758-139">Header</span><span class="sxs-lookup"><span data-stu-id="3c758-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3c758-140"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c758-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c758-141">Library</span></span><br/> | <dl> <span data-ttu-id="3c758-142"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3c758-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c758-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c758-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c758-144">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3c758-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="3c758-145">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="3c758-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




