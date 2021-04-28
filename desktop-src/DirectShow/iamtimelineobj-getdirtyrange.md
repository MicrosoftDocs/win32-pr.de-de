---
description: 'IAMTimelineObj::GetDirtyRange-Methode: Nicht unterstützt.'
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: IAMTimelineObj::GetDirtyRange-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 828bb5a88d3bcefcf10f0a6e4f07070a4b60322d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098568"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="620a4-103">IAMTimelineObj::GetDirtyRange-Methode</span><span class="sxs-lookup"><span data-stu-id="620a4-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="620a4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="620a4-104">\[Deprecated.</span></span> <span data-ttu-id="620a4-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="620a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="620a4-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="620a4-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="620a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="620a4-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="620a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="620a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="620a4-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="620a4-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="620a4-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="620a4-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="620a4-111">*Pstop*</span><span class="sxs-lookup"><span data-stu-id="620a4-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="620a4-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="620a4-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="620a4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="620a4-113">Return value</span></span>

<span data-ttu-id="620a4-114">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="620a4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="620a4-115">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="620a4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="620a4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="620a4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="620a4-117">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="620a4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="620a4-118">Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und .NET Framework [3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="620a4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="620a4-119">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="620a4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="620a4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="620a4-120">Requirements</span></span>



| <span data-ttu-id="620a4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="620a4-121">Requirement</span></span> | <span data-ttu-id="620a4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="620a4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="620a4-123">Header</span><span class="sxs-lookup"><span data-stu-id="620a4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="620a4-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="620a4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="620a4-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="620a4-125">Library</span></span><br/> | <dl> <span data-ttu-id="620a4-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="620a4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="620a4-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="620a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620a4-128">**IAMTimelineObj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="620a4-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




