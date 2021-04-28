---
description: 'IAMTimelineObj::SetDirtyRange2-Methode: Nicht implementiert.'
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: IAMTimelineObj::SetDirtyRange2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 149274a7dcb185f362ae8f58915b81af07a2bf5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098534"
---
# <a name="iamtimelineobjsetdirtyrange2-method"></a><span data-ttu-id="295e6-103">IAMTimelineObj::SetDirtyRange2-Methode</span><span class="sxs-lookup"><span data-stu-id="295e6-103">IAMTimelineObj::SetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="295e6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="295e6-104">\[Deprecated.</span></span> <span data-ttu-id="295e6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="295e6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="295e6-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="295e6-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="295e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="295e6-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="295e6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="295e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="295e6-109">*Starten*</span><span class="sxs-lookup"><span data-stu-id="295e6-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="295e6-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="295e6-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="295e6-111">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="295e6-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="295e6-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="295e6-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="295e6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="295e6-113">Return value</span></span>

<span data-ttu-id="295e6-114">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="295e6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="295e6-115">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="295e6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="295e6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="295e6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="295e6-117">Die Headerdatei Qedit.h ist mit Direct3D-Headern nach Version 7 nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="295e6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="295e6-118">Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="295e6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="295e6-119">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="295e6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="295e6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="295e6-120">Requirements</span></span>



| <span data-ttu-id="295e6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="295e6-121">Requirement</span></span> | <span data-ttu-id="295e6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="295e6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="295e6-123">Header</span><span class="sxs-lookup"><span data-stu-id="295e6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="295e6-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="295e6-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="295e6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="295e6-125">Library</span></span><br/> | <dl> <span data-ttu-id="295e6-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="295e6-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="295e6-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="295e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="295e6-128">**IAMTimelineObj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="295e6-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




