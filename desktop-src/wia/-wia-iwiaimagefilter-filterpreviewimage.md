---
description: Filtert das Vorschaubild.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Iwiaimagefilter:: FilterPreviewImage-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346999"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="380fd-103">Iwiaimagefilter:: FilterPreviewImage-Methode</span><span class="sxs-lookup"><span data-stu-id="380fd-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="380fd-104">Filtert das Vorschaubild.</span><span class="sxs-lookup"><span data-stu-id="380fd-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="380fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="380fd-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="380fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="380fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380fd-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="380fd-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="380fd-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="380fd-108">Type: **LONG**</span></span>

<span data-ttu-id="380fd-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="380fd-109">Not used.</span></span> <span data-ttu-id="380fd-110">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="380fd-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="380fd-111">*pWiaChildItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="380fd-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="380fd-112">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="380fd-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="380fd-113">Das Element, das verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="380fd-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="380fd-114">_InputImageExtents \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="380fd-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="380fd-115">Typ: **Rect**</span><span class="sxs-lookup"><span data-stu-id="380fd-115">Type: **RECT**</span></span>

<span data-ttu-id="380fd-116">Die Koordinaten (auf dem physischen Erwerbs Bereich) des Bilds, das von der Vorschau Komponente intern zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="380fd-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="380fd-117">*pinputstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="380fd-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="380fd-118">Typ: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="380fd-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="380fd-119">Ein Zeiger auf die [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle für die zwischengespeicherten Bilddaten, die gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="380fd-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380fd-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="380fd-120">Return value</span></span>

<span data-ttu-id="380fd-121">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="380fd-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="380fd-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="380fd-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="380fd-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="380fd-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="380fd-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="380fd-124">Remarks</span></span>

<span data-ttu-id="380fd-125">Nennen Sie diese Methode nicht direkt aus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="380fd-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="380fd-126">*pWiaChildItem2* muss ein untergeordnetes Element des *pWiaItem2* sein, das an [**iwiaimagefilter:: initializefilter**](-wia-iwiaimagefilter-initializefilter.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="380fd-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="380fd-127">*Inputimageextents* ist erforderlich, da der Bild Verarbeitungs Filter dafür zuständig ist, den Bildbereich auszulagern, den *pWiaChildItem2* aus den durch *pinputstream* weiter gegebenen Bilddaten repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="380fd-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="380fd-128">Eine Anwendung muss sicherstellen, dass *pWiaChildItem2* das gleiche Bildformat (WIA \_ IPA \_ -Format), Auflösung (WIA \_ \_ -IPS-xres und WIA- \_ IPS \_ ) und Bittiefe (WIA \_ IPA- \_ Tiefe) wie *pWiaItem2* bei der Übergabe an [**getnewpreview**](-wia-iwiapreview-getnewpreview.md)aufweist.</span><span class="sxs-lookup"><span data-stu-id="380fd-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="380fd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="380fd-129">Requirements</span></span>



| <span data-ttu-id="380fd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="380fd-130">Requirement</span></span> | <span data-ttu-id="380fd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="380fd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="380fd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="380fd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="380fd-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="380fd-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="380fd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="380fd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="380fd-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="380fd-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="380fd-136">Header</span><span class="sxs-lookup"><span data-stu-id="380fd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="380fd-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="380fd-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="380fd-138">IDL</span><span class="sxs-lookup"><span data-stu-id="380fd-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="380fd-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="380fd-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
