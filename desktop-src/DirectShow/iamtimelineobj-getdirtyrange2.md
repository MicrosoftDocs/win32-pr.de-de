---
description: 'IAMTimelineObj::GetDirtyRange2-Methode: Wird nicht unterstützt.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: IAMTimelineObj::GetDirtyRange2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119518"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="eb9dc-103">IAMTimelineObj::GetDirtyRange2-Methode</span><span class="sxs-lookup"><span data-stu-id="eb9dc-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="eb9dc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-104">\[Deprecated.</span></span> <span data-ttu-id="eb9dc-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="eb9dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb9dc-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9dc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb9dc-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="eb9dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb9dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9dc-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="eb9dc-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="eb9dc-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb9dc-111">*Pstop*</span><span class="sxs-lookup"><span data-stu-id="eb9dc-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="eb9dc-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9dc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb9dc-113">Return value</span></span>

<span data-ttu-id="eb9dc-114">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="eb9dc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb9dc-115">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9dc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb9dc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb9dc-117">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb9dc-118">Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und .NET Framework [3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb9dc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb9dc-119">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb9dc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb9dc-120">Requirements</span></span>



| <span data-ttu-id="eb9dc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb9dc-121">Requirement</span></span> | <span data-ttu-id="eb9dc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="eb9dc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9dc-123">Header</span><span class="sxs-lookup"><span data-stu-id="eb9dc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eb9dc-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="eb9dc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb9dc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb9dc-125">Library</span></span><br/> | <dl> <span data-ttu-id="eb9dc-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb9dc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb9dc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb9dc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9dc-128">**IAMTimelineObj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eb9dc-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




