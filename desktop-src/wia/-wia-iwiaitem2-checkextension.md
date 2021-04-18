---
description: 'Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der IWiaItem2:: GetExtension-Methode verwendet werden kann.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2:: checkextension-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357397"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="c010f-103">IWiaItem2:: checkextension-Methode</span><span class="sxs-lookup"><span data-stu-id="c010f-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="c010f-104">Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) -Methode verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c010f-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c010f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c010f-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="c010f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c010f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c010f-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c010f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c010f-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="c010f-108">Type: **LONG**</span></span>

<span data-ttu-id="c010f-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c010f-109">Currently unused.</span></span> <span data-ttu-id="c010f-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c010f-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c010f-111">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c010f-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c010f-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c010f-112">Type: **BSTR**</span></span>

<span data-ttu-id="c010f-113">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c010f-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="c010f-114">*riidextensioninterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c010f-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c010f-115">Typ: **refID**</span><span class="sxs-lookup"><span data-stu-id="c010f-115">Type: **REFIID**</span></span>

<span data-ttu-id="c010f-116">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c010f-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="c010f-117">*pbextensionist vorhanden* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c010f-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c010f-118">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="c010f-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c010f-119">Empfängt einen Zeiger auf einen _ \* bool \* \*.</span><span class="sxs-lookup"><span data-stu-id="c010f-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c010f-120"><span id="FALSE"></span><span id="false"></span>**Alarm**</span><span class="sxs-lookup"><span data-stu-id="c010f-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="c010f-121">Die angegebene Erweiterung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c010f-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c010f-122"><span id="TRUE"></span><span id="true"></span>**Fall**</span><span class="sxs-lookup"><span data-stu-id="c010f-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="c010f-123">Die angegebene Erweiterung ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c010f-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c010f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c010f-124">Return value</span></span>

<span data-ttu-id="c010f-125">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c010f-125">Type: **HRESULT**</span></span>

<span data-ttu-id="c010f-126">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c010f-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c010f-127">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c010f-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c010f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c010f-128">Remarks</span></span>

<span data-ttu-id="c010f-129">Mit dieser Methode können Anwendungen überprüfen, ob eine Erweiterung verfügbar ist, bevor Sie die [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c010f-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="c010f-130">Außerdem kann die Anwendung überprüfen, welche Erweiterungen verfügbar sind, ohne Sie gemeinsam zu erstellen, und dann entscheiden, welche Erweiterungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c010f-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="c010f-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c010f-131">Examples</span></span>

<span data-ttu-id="c010f-132">Checkimgfilter überprüft, ob der Treiber über einen Bild Verarbeitungs Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="c010f-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="c010f-133">Vor dem Aufrufen der Vorschau Komponente sollte eine Anwendung sicherstellen, dass der Treiber über einen Bild Verarbeitungs Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="c010f-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c010f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c010f-134">Requirements</span></span>



| <span data-ttu-id="c010f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c010f-135">Requirement</span></span> | <span data-ttu-id="c010f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c010f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c010f-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c010f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c010f-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c010f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c010f-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c010f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c010f-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c010f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c010f-141">Header</span><span class="sxs-lookup"><span data-stu-id="c010f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c010f-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c010f-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c010f-143">IDL</span><span class="sxs-lookup"><span data-stu-id="c010f-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c010f-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c010f-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




