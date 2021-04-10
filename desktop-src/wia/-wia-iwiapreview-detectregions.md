---
description: 'Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird, an den Filter.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: Iwiapreview::D etectregions-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214656"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="c914d-103">Iwiapreview::D etectregions-Methode</span><span class="sxs-lookup"><span data-stu-id="c914d-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="c914d-104">Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird, an den Filter.</span><span class="sxs-lookup"><span data-stu-id="c914d-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c914d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c914d-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c914d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c914d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c914d-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c914d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c914d-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="c914d-108">Type: **LONG**</span></span>

<span data-ttu-id="c914d-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c914d-109">Not used.</span></span> <span data-ttu-id="c914d-110">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c914d-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c914d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c914d-111">Return value</span></span>

<span data-ttu-id="c914d-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c914d-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c914d-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c914d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c914d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c914d-114">Return code</span></span>                                                                               | <span data-ttu-id="c914d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c914d-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c914d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c914d-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c914d-117">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c914d-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="c914d-118"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="c914d-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="c914d-119">Der Treiber unterstützt keine Segmentierung.</span><span class="sxs-lookup"><span data-stu-id="c914d-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="c914d-120"><dt>**sonst**</dt></span><span class="sxs-lookup"><span data-stu-id="c914d-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="c914d-121">Ein Standard-com-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c914d-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="c914d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c914d-122">Remarks</span></span>

<span data-ttu-id="c914d-123">Eine Anwendung muss [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) aufrufen, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c914d-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="c914d-124">Wenn die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente **iwiapreview::D etectregions** aufruft, ruft Sie den Treiber Segmentierungs Filter auf und übergibt die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle, die zuvor an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c914d-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="c914d-125">Außerdem übergibt Sie das intern zwischengespeicherte Bild an den Filter.</span><span class="sxs-lookup"><span data-stu-id="c914d-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="c914d-126">Der Segmentierungs Filter verwendet das zwischengespeicherte Bild, um die untergeordneten Blöcke zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c914d-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="c914d-127">Wenn eine Anwendung Eigenschaften der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle ändert, nachdem Sie [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)aufgerufen hat, müssen die ursprünglichen Eigenschaften wieder hergestellt werden, bevor die Anwendung **iwiapreview::D etectregions** aufruft.</span><span class="sxs-lookup"><span data-stu-id="c914d-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="c914d-128">Verwenden Sie [**getpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) und [**setpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) , um die ursprünglichen Eigenschaften wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c914d-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="c914d-129">**Iwiapreview::D etectregions** wird verwendet, um die "Unterbereiche" des zwischengespeicherten Images zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c914d-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="c914d-130">Für jeden erkannten Unterbereich wird ein neues untergeordnetes WIA 2,0-Element unter der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="c914d-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="c914d-131">Für jedes untergeordnete Element muss der Segmentierungs Filter die Werte für die folgenden WIA 2,0-Eigenschaften festlegen: WIA \_ IPS \_ xpos, WIA \_ IPS \_ yPos, WIA \_ IPS \_ xblock und WIA \_ IPS \_ yblock.</span><span class="sxs-lookup"><span data-stu-id="c914d-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="c914d-132">Mit einem erweiterten Filter werden andere WIA 2,0-Eigenschaften festgelegt, wie z. b. WIA \_ \_ -IPS deplizierung \_ X und WIA- \_ IPS- \_ deschiefe \_ Y, wenn der Treiber de-Neigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c914d-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="c914d-133">Die WIA \_ \_ -IPS xpos, WIA \_ IPS \_ yPos, WIA \_ IPS \_ xblock und WIA \_ IPS \_ yblock-Eigenschaften stellen das umgebende Rechteck des zu überprüfenden Bereichs dar.</span><span class="sxs-lookup"><span data-stu-id="c914d-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="c914d-134">Der Treiber unterstützt möglicherweise keine Segmentierung.</span><span class="sxs-lookup"><span data-stu-id="c914d-134">The driver might not support segmentation.</span></span> <span data-ttu-id="c914d-135">Vor dem Aufrufen von **iwiapreview::D etectregions** überprüft eine Anwendung in der Regel, ob der Treiber die WIA- \_ IP- \_ Segmentierungs Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c914d-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="c914d-136">Wenn die Eigenschaft nicht implementiert wird, wird die Segmentierung nicht unterstützt, und **iwiapreview::D etectregions** schlägt fehl und gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="c914d-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="c914d-137">Die Anwendung muss die untergeordneten Elemente bereinigen, die durch Aufrufen von **iwiapreview::D etectregions** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c914d-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="c914d-138">Wenn eine Anwendung z. b. einen zusätzlichen **iwiapreview::D etectregions** für dasselbe Element aufruft, muss Sie die vorherigen untergeordneten Elemente bereinigen.</span><span class="sxs-lookup"><span data-stu-id="c914d-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c914d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c914d-139">Requirements</span></span>



| <span data-ttu-id="c914d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c914d-140">Requirement</span></span> | <span data-ttu-id="c914d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c914d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c914d-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c914d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c914d-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c914d-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c914d-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c914d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c914d-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c914d-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c914d-146">Header</span><span class="sxs-lookup"><span data-stu-id="c914d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c914d-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c914d-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c914d-148">IDL</span><span class="sxs-lookup"><span data-stu-id="c914d-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c914d-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c914d-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




