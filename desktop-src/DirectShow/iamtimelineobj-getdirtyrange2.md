---
description: Wird nicht unterstützt.
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'Iamtimelineobj:: GetDirtyRange2-Methode (qedit. h)'
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
ms.openlocfilehash: 44a78366c14db35f0b90b6e09cd4851d1b0a3855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365830"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="bb969-103">Iamtimelineobj:: GetDirtyRange2-Methode</span><span class="sxs-lookup"><span data-stu-id="bb969-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="bb969-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="bb969-104">\[Deprecated.</span></span> <span data-ttu-id="bb969-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="bb969-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb969-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb969-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb969-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb969-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="bb969-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb969-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb969-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="bb969-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bb969-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="bb969-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bb969-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="bb969-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="bb969-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="bb969-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb969-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb969-113">Return value</span></span>

<span data-ttu-id="bb969-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb969-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb969-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb969-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb969-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb969-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb969-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="bb969-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb969-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="bb969-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb969-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb969-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb969-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb969-120">Requirements</span></span>



| <span data-ttu-id="bb969-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb969-121">Requirement</span></span> | <span data-ttu-id="bb969-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bb969-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb969-123">Header</span><span class="sxs-lookup"><span data-stu-id="bb969-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bb969-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="bb969-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb969-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb969-125">Library</span></span><br/> | <dl> <span data-ttu-id="bb969-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="bb969-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb969-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb969-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb969-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bb969-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




