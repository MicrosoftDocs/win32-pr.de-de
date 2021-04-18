---
description: Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'Iwiapreview:: getnewpreview-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354498"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="50e54-103">Iwiapreview:: getnewpreview-Methode</span><span class="sxs-lookup"><span data-stu-id="50e54-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="50e54-104">Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen.</span><span class="sxs-lookup"><span data-stu-id="50e54-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e54-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="50e54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e54-107">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e54-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e54-108">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="50e54-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="50e54-109">Gibt einen Zeiger auf das [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Element für das Bild an.</span><span class="sxs-lookup"><span data-stu-id="50e54-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="50e54-110">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e54-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e54-111">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="50e54-111">Type: **LONG**</span></span>

<span data-ttu-id="50e54-112">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="50e54-112">Currently unused.</span></span> <span data-ttu-id="50e54-113">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="50e54-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="50e54-114">*pwiatransfercallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e54-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e54-115">Typ: \**[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="50e54-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="50e54-116">Gibt einen Zeiger auf die [_ *iwiatransfercallback* \*](-wia-iwiatransfercallback.md) -Schnittstelle der aufrufenden Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="50e54-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e54-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50e54-117">Return value</span></span>

<span data-ttu-id="50e54-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="50e54-118">Type: **HRESULT**</span></span>

<span data-ttu-id="50e54-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="50e54-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50e54-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50e54-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e54-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50e54-121">Remarks</span></span>

<span data-ttu-id="50e54-122">Eine Anwendung muss **iwiapreview:: getnewpreview** aufrufen, bevor [**iwiapreview::D etectregions**](-wia-iwiapreview-detectregions.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50e54-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="50e54-123">**Iwiapreview:: getnewpreview** legt die [**WIA-Eigenschaft \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md) fest (und setzt Sie vor der Rückgabe zurück, es sei denn, Sie wurde zuvor festgelegt).</span><span class="sxs-lookup"><span data-stu-id="50e54-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="50e54-124">Dadurch kann der Treiber und die Hardware sowie der Bild Verarbeitungs Filter wissen, dass es sich bei dem Element um eine Vorschauversion handelt.</span><span class="sxs-lookup"><span data-stu-id="50e54-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="50e54-125">Intern erstellt die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente eine Instanz des filterverarbeitungs Filters des Treibers, indem [**GetExtension**](-wia-iwiaitem2-getextension.md) auf *pWiaItem2* aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50e54-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="50e54-126">Die WIA 2,0-Vorschau Komponente führt dies aus, wenn die Anwendung **iwiapreview:: getnewpreview** aufruft.</span><span class="sxs-lookup"><span data-stu-id="50e54-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50e54-127">Die WIA 2,0-Vorschau Komponente initialisiert auch den Filter in **iwiapreview:: getnewpreview**.</span><span class="sxs-lookup"><span data-stu-id="50e54-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50e54-128">Dieselbe Filter Instanz wird von der WIA 2,0-Vorschau Komponente während eines [**iwiapreview:: updatepreview**](-wia-iwiapreview-updatepreview.md)-Aufrufes verwendet.</span><span class="sxs-lookup"><span data-stu-id="50e54-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="50e54-129">Vor dem Aufrufen der WIA 2,0-Vorschau Komponente sollte eine Anwendung [**checkextension**](-wia-iwiaitem2-checkextension.md) aufrufen, um sicherzustellen, dass der Treiber über einen Bild Verarbeitungs Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="50e54-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="50e54-130">Er sollte **checkextension** für das Element aufrufen, das an **iwiapreview:: getnewpreview** übergeben würde.</span><span class="sxs-lookup"><span data-stu-id="50e54-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="50e54-131">Es ist nutzlos, Live-Vorschau Versionen ohne Bild Verarbeitungs Filter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="50e54-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="50e54-132">Wenn eine Anwendung **iwiapreview:: getnewpreview** für einen Treiber ohne Bild Verarbeitungs Filter aufruft, schlägt der Aufruf fehl.</span><span class="sxs-lookup"><span data-stu-id="50e54-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="50e54-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50e54-133">Examples</span></span>

<span data-ttu-id="50e54-134">Checkimgfilter überprüft, ob der Treiber über einen Bild Verarbeitungs Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="50e54-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="50e54-135">Vor dem Aufrufen der Vorschau Komponente sollte eine Anwendung sicherstellen, dass der Treiber über einen Bild Verarbeitungs Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="50e54-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="50e54-136">Downloadpreviewimage lädt Bilddaten aus dem Scanner herunter, indem die **iwiapreview:: getnewpreview** -Methode der Vorschau Komponente aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50e54-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="50e54-137">Anschließend wird detectsubregions aufgerufen, wenn der Anwendungs Benutzer den Segmentierungs Filter aufrufen möchte, der für jeden erkannten Bereich ein untergeordnetes Element unter pWiaItem2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="50e54-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="50e54-138">Siehe [**erkenctregions**](-wia-iwiasegmentationfilter-detectregions.md) für die detectsubregions-Methode, die in diesem Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50e54-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="50e54-139">In diesem Beispiel legt der Anwendungs Benutzer fest, `m_bUseSegmentationFilter` indem Sie auf ein Kontrollkästchen klicken.</span><span class="sxs-lookup"><span data-stu-id="50e54-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="50e54-140">Wenn die Anwendung dies unterstützt, sollte zuerst überprüft werden, ob der Treiber über einen Segmentierungs Filter verfügt, indem [**checkextension**](-wia-iwiaitem2-checkextension.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50e54-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="50e54-141">Unter **iwiapreview:: getnewpreview** finden Sie ein Beispiel für die checkimgfilter-Methode, das zeigt, wie dies erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="50e54-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="50e54-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50e54-142">Requirements</span></span>



| <span data-ttu-id="50e54-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50e54-143">Requirement</span></span> | <span data-ttu-id="50e54-144">Wert</span><span class="sxs-lookup"><span data-stu-id="50e54-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50e54-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50e54-145">Minimum supported client</span></span><br/> | <span data-ttu-id="50e54-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50e54-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50e54-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50e54-147">Minimum supported server</span></span><br/> | <span data-ttu-id="50e54-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50e54-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50e54-149">Header</span><span class="sxs-lookup"><span data-stu-id="50e54-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e54-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e54-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="50e54-151">IDL</span><span class="sxs-lookup"><span data-stu-id="50e54-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50e54-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50e54-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




