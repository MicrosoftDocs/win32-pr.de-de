---
description: Ruft die Erweiterungs Schnittstellen ab, die möglicherweise mit einem Windows-Abbild Erfassungs-Gerätetreiber (WIA) 2,0 geliefert werden.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2:: GetExtension-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041759"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="ace75-103">IWiaItem2:: GetExtension-Methode</span><span class="sxs-lookup"><span data-stu-id="ace75-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="ace75-104">Ruft die Erweiterungs Schnittstellen ab, die möglicherweise mit einem Windows-Abbild Erfassungs-Gerätetreiber (WIA) 2,0 geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="ace75-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace75-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="ace75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace75-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace75-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace75-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="ace75-108">Type: **LONG**</span></span>

<span data-ttu-id="ace75-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ace75-109">Currently unused.</span></span> <span data-ttu-id="ace75-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ace75-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ace75-111">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace75-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace75-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ace75-112">Type: **BSTR**</span></span>

<span data-ttu-id="ace75-113">Gibt den Namen der Erweiterung an, auf die die aufrufenden Anwendung einen Zeiger erfordert.</span><span class="sxs-lookup"><span data-stu-id="ace75-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="ace75-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**Segmentationfilter**</span><span class="sxs-lookup"><span data-stu-id="ace75-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="ace75-115">Die Segmentierungs Filter Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ace75-115">The segmentation filter extension.</span></span> <span data-ttu-id="ace75-116">Dies ist zurzeit der einzige gültige Wert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="ace75-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ace75-117">*riidextensioninterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace75-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace75-118">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="ace75-118">Type: **REFIID**</span></span>

<span data-ttu-id="ace75-119">Gibt den Bezeichner der Erweiterungsschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="ace75-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="ace75-120">*ppOut* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ace75-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace75-121">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="ace75-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="ace75-122">Empfängt die Adresse eines Zeigers auf die Erweiterungsschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ace75-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace75-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ace75-123">Return value</span></span>

<span data-ttu-id="ace75-124">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ace75-124">Type: **HRESULT**</span></span>

<span data-ttu-id="ace75-125">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ace75-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ace75-126">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ace75-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace75-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ace75-127">Remarks</span></span>

<span data-ttu-id="ace75-128">Eine Anwendung ruft diese Methode auf, um ein Erweiterungs Objekt zu erstellen, das eine der WIA 2,0-Treiber Erweiterungs Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="ace75-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="ace75-129">**IWiaItem2:: GetExtension** speichert die Adresse der Erweiterungsschnittstelle des Erweiterungs Objekts im *riidextensioninterface* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ace75-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="ace75-130">Die Anwendung verwendet dann den Schnittstellen Zeiger, um die Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ace75-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="ace75-131">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *riidextensioninterface* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="ace75-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="ace75-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ace75-132">Examples</span></span>

<span data-ttu-id="ace75-133">Createsegmentationfilter erstellt eine Instanz des Segmentierungs Filters des Treibers ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) durch Aufrufen von **IWiaItem2:: GetExtension** für die eingegangene [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ace75-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ace75-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ace75-134">Requirements</span></span>



| <span data-ttu-id="ace75-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ace75-135">Requirement</span></span> | <span data-ttu-id="ace75-136">Wert</span><span class="sxs-lookup"><span data-stu-id="ace75-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ace75-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ace75-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ace75-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace75-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ace75-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ace75-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ace75-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ace75-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ace75-141">Header</span><span class="sxs-lookup"><span data-stu-id="ace75-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace75-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace75-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="ace75-143">IDL</span><span class="sxs-lookup"><span data-stu-id="ace75-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ace75-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ace75-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
