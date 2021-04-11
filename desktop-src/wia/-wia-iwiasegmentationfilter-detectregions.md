---
description: Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Iwiasegmentationfilter::D etectregions-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129416"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="2e8b0-103">Iwiasegmentationfilter::D etectregions-Methode</span><span class="sxs-lookup"><span data-stu-id="2e8b0-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="2e8b0-104">Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e8b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e8b0-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="2e8b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e8b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e8b0-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e8b0-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8b0-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-108">Type: **LONG**</span></span>

<span data-ttu-id="2e8b0-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-109">Currently unused.</span></span> <span data-ttu-id="2e8b0-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="2e8b0-111">*pinputstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e8b0-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8b0-112">Typ: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="2e8b0-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="2e8b0-113">Gibt einen Zeiger auf das [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Vorschaubild an.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="2e8b0-114">_pWiaItem2 \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e8b0-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8b0-115">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="2e8b0-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="2e8b0-116">Gibt einen Zeiger auf das [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Element an, für das *pinputstream abgerufen* wurde.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="2e8b0-117">Der Segmentierungs Filter erstellt untergeordnete Elemente für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e8b0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e8b0-118">Return value</span></span>

<span data-ttu-id="2e8b0-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-119">Type: **HRESULT**</span></span>

<span data-ttu-id="2e8b0-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e8b0-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e8b0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e8b0-122">Remarks</span></span>

<span data-ttu-id="2e8b0-123">Diese Methode bestimmt die Unterbereiche des durch pinputstream dargestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="2e8b0-124">Für jede unterregion, die Sie erkennt, wird ein untergeordnetes Element für das [**IWiaItem2**](-wia-iwiaitem2.md) -Element erstellt, das im *pWiaItem2* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="2e8b0-125">Für jedes untergeordnete Element muss der Segmentierungs Filter Werte für das umgebende Rechteck des zu überprüfenden Bereichs festlegen, wobei die folgenden [**Eigenschaften Konstanten für die WIA-Eigenschaft des Scanners**](-wia-wiaitempropscanneritem.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="2e8b0-126">**WIA- \_ IPS- \_ xPos**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="2e8b0-127">**WIA- \_ IPS ( \_ yPos)**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="2e8b0-128">**WIA- \_ IPS- \_ XBlock**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="2e8b0-129">**WIA- \_ IPS \_ yblock**</span><span class="sxs-lookup"><span data-stu-id="2e8b0-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="2e8b0-130">Ein erweiterter Filter erfordert möglicherweise auch andere [**Scanner-WIA-Element Eigenschafts Konstanten**](-wia-wiaitempropscanneritem.md) , wie z. b. **WIA- \_ IPS \_ deschiefe \_ X** und **WIA- \_ IPS \_ deschiefe \_ Y**, wenn der Treiber de-Schiefe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="2e8b0-131">Wenn die Anwendung **iwiasegmentationfilter::D etectregions** mehrmals aufruft, muss die Anwendung zunächst die untergeordneten Elemente löschen, die beim letzten Aufruf von **iwiasegmentationfilter::D etectregions** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="2e8b0-132">Wenn eine Anwendung Eigenschaften in *pWiaItem2* ändert, muss zwischen dem Abrufen des Bilds in *pinputstream* und dem Aufruf von **iwiasegmentationfilter::D etectregions** die ursprünglichen Eigenschaften (d. h. die Eigenschaften, die das Element beim Abrufen des Streams enthielt) wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="2e8b0-133">Dies kann durch [**getpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) und [**setpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="2e8b0-134">Die Anwendung muss den [IStream](/windows/win32/api/objidl/nn-objidl-istream) zurücksetzen, wenn der zugehörige-Befehl denselben Stream mehrmals an den Segmentierungs Filter übergibt.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="2e8b0-135">Die Anwendung muss den Stream auch nach dem anfänglichen Download und vor dem Aufrufen von **iwiasegmentationfilter::D etectregions** zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="2e8b0-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e8b0-136">Examples</span></span>

<span data-ttu-id="2e8b0-137">Die Segmentierung führt die Regions Erkennung im Stream () aus, die an `pImageStream` detectsubregions weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="2e8b0-138">Weitere Informationen finden Sie in diesem Beispiel in der [**GetExtension**](-wia-iwiaitem2-getextension.md) für die in diesem Beispiel verwendete Methode "".</span><span class="sxs-lookup"><span data-stu-id="2e8b0-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="2e8b0-139">Downloadpreviewimage lädt Bilddaten aus dem Scanner herunter, indem die [**getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode der Vorschau Komponente aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="2e8b0-140">Anschließend wird detectsubregions aufgerufen, wenn der Anwendungs Benutzer den Segmentierungs Filter aufrufen möchte, der für jeden erkannten Bereich ein untergeordnetes Element unter pWiaItem2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="2e8b0-141">Weitere Informationen finden Sie unter **iwiasegmentationfilter::D etectregions** für die detectsubregions-Methode, die in diesem Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="2e8b0-142">In diesem Beispiel legt der Anwendungs Benutzer fest, `m_bUseSegmentationFilter` indem Sie auf ein Kontrollkästchen klicken.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="2e8b0-143">Wenn die Anwendung dies unterstützt, sollte zuerst überprüft werden, ob der Treiber über einen Segmentierungs Filter verfügt, indem [**checkextension**](-wia-iwiaitem2-checkextension.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="2e8b0-144">Unter [**getnewpreview**](-wia-iwiapreview-getnewpreview.md) finden Sie ein Beispiel für die checkimgfilter-Methode, das zeigt, wie dies erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="2e8b0-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e8b0-145">Requirements</span></span>



| <span data-ttu-id="2e8b0-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e8b0-146">Requirement</span></span> | <span data-ttu-id="2e8b0-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2e8b0-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8b0-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e8b0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2e8b0-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e8b0-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e8b0-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e8b0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2e8b0-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e8b0-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e8b0-152">Header</span><span class="sxs-lookup"><span data-stu-id="2e8b0-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e8b0-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e8b0-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e8b0-154">IDL</span><span class="sxs-lookup"><span data-stu-id="2e8b0-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e8b0-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e8b0-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
