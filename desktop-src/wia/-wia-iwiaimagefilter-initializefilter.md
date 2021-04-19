---
description: Initialisiert den Filter. Wird von der Windows-Abbild Beschaffung (WIA) 2,0 vor jedem Herunterladen des Images aufgerufen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Iwiaimagefilter:: initializefilter-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359059"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="42819-104">Iwiaimagefilter:: initializefilter-Methode</span><span class="sxs-lookup"><span data-stu-id="42819-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="42819-105">Initialisiert den Filter.</span><span class="sxs-lookup"><span data-stu-id="42819-105">Initializes the filter.</span></span> <span data-ttu-id="42819-106">Wird von der Windows-Abbild Beschaffung (WIA) 2,0 vor jedem Herunterladen des Images aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="42819-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="42819-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42819-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="42819-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42819-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42819-109">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42819-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42819-110">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="42819-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="42819-111">Gibt einen Zeiger auf das [_ *IWiaItem2* \*](-wia-iwiaitem2.md) -Element an, das das Vorschaubild darstellt.</span><span class="sxs-lookup"><span data-stu-id="42819-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="42819-112">*pwiatransfercallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42819-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42819-113">Typ: \**[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="42819-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="42819-114">Gibt einen Zeiger auf die [_ *iwiatransfercallback* \*](-wia-iwiatransfercallback.md) -Schnittstelle der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="42819-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42819-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42819-115">Return value</span></span>

<span data-ttu-id="42819-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42819-116">Type: **HRESULT**</span></span>

<span data-ttu-id="42819-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="42819-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42819-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="42819-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42819-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42819-119">Remarks</span></span>

<span data-ttu-id="42819-120">Diese Methode wird aufgerufen, wenn eine Anwendung den [**Download**](-wia-iwiatransfer-download.md) aufruft und eine Anwendung die Funktion der WIA 2,0-Vorschau Komponente aufruft `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="42819-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="42819-121">**Iwiaimagefilter:: initializefilter** speichert die Verweise auf *pWiaItem2* und *pwiatransfercallback* , um diese Funktionen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="42819-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="42819-122">Diese beiden Schnittstellen Zeiger sollten als Element Variablen gespeichert werden, und [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sollte für jede aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="42819-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="42819-123">Die Schnittstellen Zeiger werden auch in der Implementierung von " [**transfercallback**](-wia-iwiatransfercallback-transfercallback.md) " und " [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) " des Filters während der Abbild Erfassung benötigt.</span><span class="sxs-lookup"><span data-stu-id="42819-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="42819-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42819-124">Requirements</span></span>



| <span data-ttu-id="42819-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42819-125">Requirement</span></span> | <span data-ttu-id="42819-126">Wert</span><span class="sxs-lookup"><span data-stu-id="42819-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42819-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42819-127">Minimum supported client</span></span><br/> | <span data-ttu-id="42819-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42819-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42819-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42819-129">Minimum supported server</span></span><br/> | <span data-ttu-id="42819-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42819-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42819-131">Header</span><span class="sxs-lookup"><span data-stu-id="42819-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="42819-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="42819-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="42819-133">IDL</span><span class="sxs-lookup"><span data-stu-id="42819-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42819-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42819-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
