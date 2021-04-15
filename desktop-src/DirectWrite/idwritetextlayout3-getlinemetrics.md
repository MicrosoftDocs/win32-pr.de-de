---
title: IDWriteTextLayout3 getLineMetrics-Methode
description: Ruft die Eigenschaften der einzelnen Zeilen ab.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- GetLineMetrics-Methode direkt schreiben
- GetLineMetrics-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, getLineMetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477517"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="2cd81-106">IDWriteTextLayout3:: getLineMetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="2cd81-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="2cd81-107">Ruft die Eigenschaften der einzelnen Zeilen ab.</span><span class="sxs-lookup"><span data-stu-id="2cd81-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd81-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cd81-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="2cd81-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cd81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd81-110">*linemetriken* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cd81-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd81-111">Das Array, das mit Zeilen Informationen aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cd81-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="2cd81-112">*MaxLineCount*</span><span class="sxs-lookup"><span data-stu-id="2cd81-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="2cd81-113">Die maximale Größe des LineMetrics-Arrays.</span><span class="sxs-lookup"><span data-stu-id="2cd81-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="2cd81-114">*actuallinecount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cd81-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd81-115">Die tatsächliche Größe des benötigten LineMetrics-Arrays.</span><span class="sxs-lookup"><span data-stu-id="2cd81-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd81-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cd81-116">Return value</span></span>

<span data-ttu-id="2cd81-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2cd81-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cd81-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cd81-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd81-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cd81-119">Remarks</span></span>

<span data-ttu-id="2cd81-120">Wenn MaxLineCount nicht groß genug \_ \_ und kein ausreichender \_ Puffer ist, der HRESULT \_ aus \_ Win32 (Fehler \_ unzureichender \_ Puffer) entspricht, wird zurückgegeben, und actuallinecount wird auf die Anzahl der benötigten Zeilen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cd81-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd81-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cd81-121">Requirements</span></span>



| <span data-ttu-id="2cd81-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cd81-122">Requirement</span></span> | <span data-ttu-id="2cd81-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2cd81-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd81-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cd81-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2cd81-125">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2cd81-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2cd81-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cd81-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2cd81-127">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd81-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2cd81-128">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="2cd81-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2cd81-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd81-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2cd81-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cd81-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cd81-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cd81-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2cd81-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd81-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cd81-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd81-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2cd81-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cd81-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd81-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="2cd81-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





