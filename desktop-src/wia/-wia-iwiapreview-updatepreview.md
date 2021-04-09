---
description: 'Ruft das ungefilterte Bild ab, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Iwiapreview:: updatepreview-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129417"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="281c9-103">Iwiapreview:: updatepreview-Methode</span><span class="sxs-lookup"><span data-stu-id="281c9-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="281c9-104">Ruft das ungefilterte Bild ab, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="281c9-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="281c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="281c9-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="281c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="281c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281c9-107">*loptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="281c9-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="281c9-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="281c9-108">Type: **LONG**</span></span>

<span data-ttu-id="281c9-109">Gibt an, ob die Anwendung die WIA 2,0-Vorschau Komponente benötigt, um einen Teilbereich des zwischengespeicherten Bilds oder das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="281c9-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="281c9-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**Wiapreviewreturnoriginalimage**</span><span class="sxs-lookup"><span data-stu-id="281c9-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="281c9-111">Übergeben Sie das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter.</span><span class="sxs-lookup"><span data-stu-id="281c9-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="281c9-112">*pchildwiaitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="281c9-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="281c9-113">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="281c9-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="281c9-114">Gibt einen Zeiger auf das [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Element an, das ein untergeordnetes Element des **IWiaItem2** -Elements ist, das durch den *pWiaItem2* -Parameter der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="281c9-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="281c9-115">Wenn die Anwendung eine Vorschau des gesamten Flatbed erfordert, gibt einen Zeiger auf den *pWiaItem2* -Parameter der **iwiapreview:: getnewpreview** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="281c9-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="281c9-116">Wenn *pchildwiaitem* ein untergeordnetes Element des *pWiaItem2* -Parameters von **iwiapreview:: getnewpreview** ist, wird dieses untergeordnete Element normalerweise vom Segmentierungs Filter erstellt.</span><span class="sxs-lookup"><span data-stu-id="281c9-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281c9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="281c9-117">Return value</span></span>

<span data-ttu-id="281c9-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="281c9-118">Type: **HRESULT**</span></span>

<span data-ttu-id="281c9-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="281c9-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="281c9-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="281c9-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="281c9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="281c9-121">Remarks</span></span>

<span data-ttu-id="281c9-122">Diese Methode übergibt das zwischengespeicherte, ungefilterte Bild über den Bild Verarbeitungs Filter, der dann die gefilterten Daten in den von der Anwendung bereitgestellten Stream schreibt.</span><span class="sxs-lookup"><span data-stu-id="281c9-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="281c9-123">Die WIA 2,0-Vorschau Komponente ruft diesen Stream durch Aufrufen der [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) -Methode des Bild Verarbeitungs Filters ab, die dann die **getnextstream** -Implementierung des Anwendungs Rückrufs aufruft.</span><span class="sxs-lookup"><span data-stu-id="281c9-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="281c9-124">Vor dem Aufrufen von **iwiapreview:: updatepreview** muss eine Anwendung zuerst [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) aufrufen, um das Image vom Scanner abzurufen. Andernfalls gibt die Methode einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="281c9-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="281c9-125">Die WIA 2,0-Vorschau Komponente speichert das ungefilterte Bild, das vom Treiber heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="281c9-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="281c9-126">Es ist möglich, dass das an **iwiapreview:: updatepreview** übergebenen WIA 2,0-Element nur einen kleinen Bereich des vom Treiber heruntergeladenen Bilds darstellt.</span><span class="sxs-lookup"><span data-stu-id="281c9-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="281c9-127">Wenn dies der Fall ist, schneidet die WIA 2,0-Vorschau Komponente diese Region tatsächlich aus dem zwischengespeicherten Image aus, bevor Sie Sie an den Bild Verarbeitungs Filter übergibt, der wiederum die gefilterten Bilddaten an die Anwendung zurück übergibt.</span><span class="sxs-lookup"><span data-stu-id="281c9-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="281c9-128">Damit eine Anwendung das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter übergibt (der wiederum an die Anwendung übergeben wird), muss die *loptions* beim Aufrufen von **iwiapreview:: updatepreview** auf **wiapreviewreturnoriginalimage** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="281c9-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="281c9-129">Wenn *loptions* auf **wiapreviewreturnoriginalimage** festgelegt wird, muss die Anwendung sicherstellen, dass die Block Einstellungen ([**WIA \_ IPS \_ xblock**](-wia-wiaitempropscanneritem.md) und **WIA \_ IPS \_ yblock**) des an **iwiapreview:: updatepreview** übergebenen Elements mit dem vollständig zwischengespeicherten Image übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="281c9-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="281c9-130">Der Bild Verarbeitungs Filter muss in diesem Fall nichts unterscheiden. das Image wird einfach basierend auf den Eigenschaften von *pchildwiaitem* gefiltert (in diesem Fall ist *pchildwiaitem* dasselbe Element, das an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben wurde).</span><span class="sxs-lookup"><span data-stu-id="281c9-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="281c9-131">Die Unterbereiche werden ignoriert, und das gesamte Bild wird mit denselben Einstellungen gefiltert.</span><span class="sxs-lookup"><span data-stu-id="281c9-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="281c9-132">Es gibt mehrere Gründe, warum eine Anwendung dies tun würde.</span><span class="sxs-lookup"><span data-stu-id="281c9-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="281c9-133">Die Anwendung unterstützt möglicherweise nicht das Ändern der Einstellungen (z. b. durch [**WIA- \_ IPS- \_ Helligkeit**](-wia-wiaitempropscanneritem.md) und **WIA- \_ IPS \_**) für jede Region, die der Segmentierungs Filter erkennt (oder der Segmentierungs Filter kann nicht einmal verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="281c9-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="281c9-134">Es ist einfacher, dass die Anwendung **iwiapreview:: updatepreview** mit **wiapreviewreturnoriginalimage** aufruft, damit Sie immer das vollständige Image aus der WIA 2,0 Preview-Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="281c9-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="281c9-135">Die WIA 2,0 Preview-Komponente unterstützt das Bildformat des Vorschaubilds nicht. in diesem Fall können die Aktionen nicht zum Ausschneiden der gewünschten Region durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="281c9-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="281c9-136">Die Unterstützung von Image Formaten der WIA 2,0 Preview-Komponente ist auf Formate beschränkt, für die Windows GDI+ 1,1 Encoder und Decoders vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="281c9-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="281c9-137">Diese Formate sind Bitmap (BMP) (eine Bitmap, die den BITMAPFILEHEADER enthält), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="281c9-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="281c9-138">Beachten Sie Folgendes: Wenn die Anwendung **wiapreviewreturnoriginalimage** an **iwiapreview:: updatepreview** übergibt, kann die WIA 2,0-Vorschau Komponente jedes beliebige Bild oder Pixel Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="281c9-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="281c9-139">**Iwiapreview:: updatepreview** legt die [**WIA-Eigenschaft \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md) fest (und setzt Sie vor der Rückgabe zurück, es sei denn, Sie wurde zuvor festgelegt).</span><span class="sxs-lookup"><span data-stu-id="281c9-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="281c9-140">Dadurch kann der Treiber (und die Hardware) und der Bild Verarbeitungs Filter wissen, dass es sich bei dem Element um eine Vorschauversion handelt.</span><span class="sxs-lookup"><span data-stu-id="281c9-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="281c9-141">Eine Anwendung muss sicherstellen, dass *pchildwiaitem* über das gleiche Bildformat ([**WIA \_ IPA- \_ Format**](-wia-wiaitempropcommonitem.md)) und die Auflösung ([**WIA- \_ IPS \_ xres**](-wia-wiaitempropscanneritem.md) und **WIA- \_ IPS \_**) wie *pwiaitem* verfügt, als es an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="281c9-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="281c9-142">Das Format des untergeordneten Elements muss dem Format des zwischengespeicherten Images der WIA 2,0-Vorschau Komponente entsprechen (die WIA 2,0 Preview-Komponente führt keine Bild Konvertierung aus).</span><span class="sxs-lookup"><span data-stu-id="281c9-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="281c9-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="281c9-143">Examples</span></span>

<span data-ttu-id="281c9-144">Updateregion sollte jedes Mal aufgerufen werden, wenn sich ein Benutzer ändert, z. b. die Helligkeit oder der Kontrast für das untergeordnete Element, das durch dargestellt wird `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="281c9-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="281c9-145">Dieses untergeordnete Element wurde zuvor vom Segmentierungs Filter ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) erstellt.</span><span class="sxs-lookup"><span data-stu-id="281c9-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="281c9-146">Das in [IStream](/windows/win32/api/objidl/nn-objidl-istream) geschriebene Bild wird von der [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) -Methode der Übertragungs Rückruf Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="281c9-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="281c9-147">Der Code für "getsubregionitem" wird in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="281c9-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="281c9-148">Nachdem diese Funktion aufgerufen wurde, würde eine Anwendung in der Regel den Bereich auf dem Bildschirm neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="281c9-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="281c9-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="281c9-149">Requirements</span></span>



| <span data-ttu-id="281c9-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="281c9-150">Requirement</span></span> | <span data-ttu-id="281c9-151">Wert</span><span class="sxs-lookup"><span data-stu-id="281c9-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="281c9-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="281c9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="281c9-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="281c9-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="281c9-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="281c9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="281c9-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="281c9-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="281c9-156">Header</span><span class="sxs-lookup"><span data-stu-id="281c9-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="281c9-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="281c9-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="281c9-158">IDL</span><span class="sxs-lookup"><span data-stu-id="281c9-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="281c9-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="281c9-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
