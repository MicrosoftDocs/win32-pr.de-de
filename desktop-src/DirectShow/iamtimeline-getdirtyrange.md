---
description: 'IAMTimeline::GetDirtyRange-Methode: Wird nicht unterstützt.'
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: IAMTimeline::GetDirtyRange-Methode (Qedit.h)
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
ms.openlocfilehash: cb0ecbd8a93698d36354c251f0381c35acf288a2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119598"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="6c5b8-103">IAMTimeline::GetDirtyRange-Methode</span><span class="sxs-lookup"><span data-stu-id="6c5b8-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="6c5b8-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-104">\[Deprecated.</span></span> <span data-ttu-id="6c5b8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6c5b8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6c5b8-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c5b8-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6c5b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c5b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5b8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="6c5b8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5b8-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6c5b8-111">*Pstop*</span><span class="sxs-lookup"><span data-stu-id="6c5b8-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6c5b8-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5b8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c5b8-113">Return value</span></span>

<span data-ttu-id="6c5b8-114">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c5b8-115">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c5b8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c5b8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c5b8-117">Die Headerdatei Qedit.h ist mit Direct3D-Headern nach Version 7 nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c5b8-118">Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6c5b8-119">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c5b8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5b8-120">Requirements</span></span>



| <span data-ttu-id="6c5b8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5b8-121">Requirement</span></span> | <span data-ttu-id="6c5b8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5b8-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5b8-123">Header</span><span class="sxs-lookup"><span data-stu-id="6c5b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6c5b8-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5b8-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6c5b8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c5b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="6c5b8-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c5b8-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5b8-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c5b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5b8-128">**IAMTimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6c5b8-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




