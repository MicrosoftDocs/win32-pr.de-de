---
title: IDWriteTextLayout2 getmetrics-Methode
description: Ruft allgemeine Metriken für die formatierte Zeichenfolge ab.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Getmetrics-Methode direkt schreiben
- Getmetrics-Methode Direct Write, IDWriteTextLayout2-Schnittstelle
- IDWriteTextLayout2 Interface Direct Write, getmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341398"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="50447-106">IDWriteTextLayout2:: getmetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="50447-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="50447-107">Ruft allgemeine Metriken für die formatierte Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="50447-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="50447-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="50447-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="50447-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50447-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="50447-110">*TextMetrics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50447-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50447-111">Typ: \**[**dwrite \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="50447-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="50447-112">Wenn diese Methode zurückgegeben wird, enthält Sie die gemessenen Abstände von Text und zugeordneter Inhalt nach dem formatieren.</span><span class="sxs-lookup"><span data-stu-id="50447-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50447-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50447-113">Return value</span></span>

<span data-ttu-id="50447-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="50447-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="50447-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="50447-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50447-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50447-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50447-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50447-117">Requirements</span></span>



| <span data-ttu-id="50447-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50447-118">Requirement</span></span> | <span data-ttu-id="50447-119">Wert</span><span class="sxs-lookup"><span data-stu-id="50447-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50447-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50447-120">Minimum supported client</span></span><br/> | <span data-ttu-id="50447-121">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="50447-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="50447-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50447-122">Minimum supported server</span></span><br/> | <span data-ttu-id="50447-123">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="50447-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="50447-124">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="50447-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="50447-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="50447-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="50447-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50447-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="50447-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50447-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="50447-128">DLL</span><span class="sxs-lookup"><span data-stu-id="50447-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50447-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50447-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50447-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50447-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50447-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="50447-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





