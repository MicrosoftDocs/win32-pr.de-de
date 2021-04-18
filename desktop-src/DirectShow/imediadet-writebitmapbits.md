---
description: Die "Write-Bitmapbits"-Methode ruft einen Video Frame zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei. Der Videoframe weist immer das 24-Bit-RGB-Format auf.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Imediadet:: Beschreib tebitmapbits-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352975"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="8ac00-104">Imediadet:: schreitebitmapbits-Methode</span><span class="sxs-lookup"><span data-stu-id="8ac00-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="8ac00-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8ac00-105">\[Deprecated.</span></span> <span data-ttu-id="8ac00-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8ac00-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ac00-107">Die `WriteBitmapBits` -Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8ac00-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="8ac00-108">Der Videoframe weist immer das 24-Bit-RGB-Format auf.</span><span class="sxs-lookup"><span data-stu-id="8ac00-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac00-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac00-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="8ac00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac00-111">*Streamtime*</span><span class="sxs-lookup"><span data-stu-id="8ac00-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac00-112">Der Zeitpunkt, zu dem der Videoframe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ac00-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="8ac00-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="8ac00-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac00-114">Breite des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8ac00-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8ac00-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="8ac00-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac00-116">Höhe des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8ac00-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8ac00-117">*Filename*</span><span class="sxs-lookup"><span data-stu-id="8ac00-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac00-118">Der Pfad der Datei, in der die Bitmap gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ac00-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="8ac00-119">Wenn die Datei bereits vorhanden ist, wird Sie von dieser Methode überschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ac00-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac00-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ac00-120">Return value</span></span>

<span data-ttu-id="8ac00-121">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8ac00-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="8ac00-122">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="8ac00-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="8ac00-123">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="8ac00-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="8ac00-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8ac00-124">Return code</span></span>                                                                                             | <span data-ttu-id="8ac00-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ac00-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ac00-126"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="8ac00-127">Der [**Sample Grabber**](sample-grabber-filter.md) -Filter konnte dem Diagramm nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8ac00-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="8ac00-128"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="8ac00-129">Fehler.</span><span class="sxs-lookup"><span data-stu-id="8ac00-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="8ac00-130"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="8ac00-131">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8ac00-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="8ac00-132"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="8ac00-133">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8ac00-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="8ac00-134"><dt>**STG \_ E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="8ac00-135">Datei kann nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8ac00-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="8ac00-136"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="8ac00-137">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="8ac00-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8ac00-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ac00-138">Remarks</span></span>

<span data-ttu-id="8ac00-139">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="8ac00-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="8ac00-140">Mit dieser Methode wird der Medien Detektor in den bitmapingmodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="8ac00-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="8ac00-141">Nachdem diese Methode aufgerufen wurde, funktionieren die verschiedenen Datenstrom Informationsmethoden in **imediadet** nicht, es sei denn, Sie erstellen eine neue Instanz des Medien Detektors.</span><span class="sxs-lookup"><span data-stu-id="8ac00-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="8ac00-142">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8ac00-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ac00-143">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8ac00-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ac00-144">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8ac00-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ac00-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ac00-145">Requirements</span></span>



| <span data-ttu-id="8ac00-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ac00-146">Requirement</span></span> | <span data-ttu-id="8ac00-147">Wert</span><span class="sxs-lookup"><span data-stu-id="8ac00-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac00-148">Header</span><span class="sxs-lookup"><span data-stu-id="8ac00-148">Header</span></span><br/>  | <dl> <span data-ttu-id="8ac00-149"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ac00-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ac00-150">Library</span></span><br/> | <dl> <span data-ttu-id="8ac00-151"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="8ac00-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac00-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ac00-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac00-153">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ac00-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="8ac00-154">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="8ac00-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




