---
description: 'Wird nicht unterstützt. Aufrufen der iamtimelinecomp:: getrecursivelayeroftype-Methode.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Iamtimelinecomp:: getrecursivelayeroftypei-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371048"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="cf7d9-104">Iamtimelinecomp:: getrecursivelayeroftypei-Methode</span><span class="sxs-lookup"><span data-stu-id="cf7d9-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="cf7d9-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-105">\[Deprecated.</span></span> <span data-ttu-id="cf7d9-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cf7d9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf7d9-107">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-107">Not supported.</span></span> <span data-ttu-id="cf7d9-108">Aufrufen der [**iamtimelinecomp:: getrecursivelayeroftype**](iamtimelinecomp-getrecursivelayeroftype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7d9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf7d9-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="cf7d9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf7d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7d9-111">*ppvirtualtrack*</span><span class="sxs-lookup"><span data-stu-id="cf7d9-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7d9-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="cf7d9-113">*pwhichlayer*</span><span class="sxs-lookup"><span data-stu-id="cf7d9-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7d9-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="cf7d9-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="cf7d9-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7d9-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7d9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf7d9-117">Return value</span></span>

<span data-ttu-id="cf7d9-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf7d9-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf7d9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf7d9-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf7d9-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf7d9-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf7d9-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf7d9-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf7d9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf7d9-124">Requirements</span></span>



| <span data-ttu-id="cf7d9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf7d9-125">Requirement</span></span> | <span data-ttu-id="cf7d9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7d9-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7d9-127">Header</span><span class="sxs-lookup"><span data-stu-id="cf7d9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cf7d9-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cf7d9-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf7d9-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf7d9-129">Library</span></span><br/> | <dl> <span data-ttu-id="cf7d9-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cf7d9-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf7d9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf7d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7d9-132">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cf7d9-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




