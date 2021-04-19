---
description: Wird nicht unterstützt.
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: 'Iamtimeline:: getdirtyrange-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2eb0c830e7bdf441432130785e1e5397d1d4267e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370256"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="b1ea7-103">Iamtimeline:: getdirtyrange-Methode</span><span class="sxs-lookup"><span data-stu-id="b1ea7-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="b1ea7-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-104">\[Deprecated.</span></span> <span data-ttu-id="b1ea7-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b1ea7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1ea7-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ea7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1ea7-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="b1ea7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1ea7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ea7-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="b1ea7-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ea7-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b1ea7-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="b1ea7-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ea7-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ea7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1ea7-113">Return value</span></span>

<span data-ttu-id="b1ea7-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1ea7-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ea7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1ea7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1ea7-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1ea7-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1ea7-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1ea7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1ea7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1ea7-120">Requirements</span></span>



| <span data-ttu-id="b1ea7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1ea7-121">Requirement</span></span> | <span data-ttu-id="b1ea7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b1ea7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ea7-123">Header</span><span class="sxs-lookup"><span data-stu-id="b1ea7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b1ea7-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b1ea7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1ea7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1ea7-125">Library</span></span><br/> | <dl> <span data-ttu-id="b1ea7-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b1ea7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ea7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1ea7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ea7-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b1ea7-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




