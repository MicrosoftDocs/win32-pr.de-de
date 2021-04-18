---
description: Die getbitmapbits-Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab. Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Imediadet:: getbitmapbits-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371291"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="1ee2e-104">Imediadet:: getbitmapbits-Methode</span><span class="sxs-lookup"><span data-stu-id="1ee2e-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="1ee2e-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-105">\[Deprecated.</span></span> <span data-ttu-id="1ee2e-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1ee2e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1ee2e-107">Die- `GetBitmapBits` Methode ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="1ee2e-108">Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee2e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ee2e-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="1ee2e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ee2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee2e-111">*Streamtime*</span><span class="sxs-lookup"><span data-stu-id="1ee2e-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee2e-112">Der Zeitpunkt, zu dem der Videoframe abgerufen werden soll (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="1ee2e-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1ee2e-113">*pbuffersize*</span><span class="sxs-lookup"><span data-stu-id="1ee2e-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee2e-114">Empfängt die erforderliche Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-114">Receives the required buffer size.</span></span> <span data-ttu-id="1ee2e-115">Wenn *pbuffer* den Wert **null** hat, erhält die Variable die Größe des Puffers, der zum Abrufen des Frames benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="1ee2e-116">Wenn *pbuffer* nicht **null** ist, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1ee2e-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="1ee2e-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee2e-118">Ein Zeiger auf einen Puffer, der eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gefolgt von den DIB-Bits empfängt.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="1ee2e-119">*Width*</span><span class="sxs-lookup"><span data-stu-id="1ee2e-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee2e-120">Breite des Video Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1ee2e-121">*Height*</span><span class="sxs-lookup"><span data-stu-id="1ee2e-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee2e-122">Höhe des Video Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee2e-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ee2e-123">Return value</span></span>

<span data-ttu-id="1ee2e-124">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ee2e-125">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="1ee2e-125">Possible values include the following:</span></span>



| <span data-ttu-id="1ee2e-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1ee2e-126">Return code</span></span>                                                                                             | <span data-ttu-id="1ee2e-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ee2e-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ee2e-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="1ee2e-129">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="1ee2e-130"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="1ee2e-131">Der [**Sample Grabber**](sample-grabber-filter.md) -Filter konnte dem Diagramm nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="1ee2e-132"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="1ee2e-133">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="1ee2e-134"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="1ee2e-135">**Null** -Zeiger Fehler.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="1ee2e-136"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="1ee2e-137">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="1ee2e-138"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="1ee2e-139">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="1ee2e-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ee2e-140">Remarks</span></span>

<span data-ttu-id="1ee2e-141">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="1ee2e-142">Um die Größe des erforderlichen Puffers zu bestimmen, müssen Sie diese Methode mit *pbuffer* gleich **null** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="1ee2e-143">Die Größe wird in der Variablen zurückgegeben, auf die von *pbuffersize* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="1ee2e-144">Erstellen Sie dann den Puffer, und rufen Sie die Methode erneut auf, wobei *pbuffer* gleich der Adresse des Puffers ist.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="1ee2e-145">Wenn die Methode zurückgegeben wird, enthält der Puffer eine **BITMAPINFOHEADER** -Struktur gefolgt von der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="1ee2e-146">Die Bitmap wird auf die Dimensionen skaliert, die in den Parametern *Width* und *height* angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="1ee2e-147">Mit dieser Methode wird der Medien Detektor in den bitmapingmodus versetzt.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="1ee2e-148">Nachdem diese Methode aufgerufen wurde, funktionieren die verschiedenen Datenstrom Informationsmethoden in **imediadet** nicht, es sei denn, Sie erstellen eine neue Instanz des Medien Detektors.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="1ee2e-149">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ee2e-150">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ee2e-151">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1ee2e-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ee2e-152">Examples</span></span>

<span data-ttu-id="1ee2e-153">Im folgenden Code wird die `GetBitmapBits` -Methode verwendet, um eine geräteunabhängige Bitmap zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="1ee2e-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ee2e-154">Requirements</span></span>



| <span data-ttu-id="1ee2e-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ee2e-155">Requirement</span></span> | <span data-ttu-id="1ee2e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee2e-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee2e-157">Header</span><span class="sxs-lookup"><span data-stu-id="1ee2e-157">Header</span></span><br/>  | <dl> <span data-ttu-id="1ee2e-158"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ee2e-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ee2e-159">Library</span></span><br/> | <dl> <span data-ttu-id="1ee2e-160"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2e-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee2e-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ee2e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee2e-162">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1ee2e-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="1ee2e-163">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="1ee2e-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




