---
description: 'IAMTimelineObj::SetSubObject-Methode: Nicht unterstützt.'
ms.assetid: a74db99b-d7ee-49df-84f1-a84e7a2f7d92
title: IAMTimelineObj::SetSubObject-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b93d95f2381f4f894cbda1edbff5d9262b7be93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098508"
---
# <a name="iamtimelineobjsetsubobject-method"></a><span data-ttu-id="fa32f-103">IAMTimelineObj::SetSubObject-Methode</span><span class="sxs-lookup"><span data-stu-id="fa32f-103">IAMTimelineObj::SetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="fa32f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fa32f-104">\[Deprecated.</span></span> <span data-ttu-id="fa32f-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="fa32f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa32f-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa32f-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa32f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa32f-107">Syntax</span></span>


```C++
HRESULT SetSubObject(
   IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fa32f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa32f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa32f-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="fa32f-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fa32f-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="fa32f-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa32f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa32f-111">Return value</span></span>

<span data-ttu-id="fa32f-112">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="fa32f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa32f-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa32f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa32f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa32f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa32f-115">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fa32f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa32f-116">Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und .NET Framework [3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa32f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa32f-117">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa32f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa32f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa32f-118">Requirements</span></span>



| <span data-ttu-id="fa32f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa32f-119">Requirement</span></span> | <span data-ttu-id="fa32f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fa32f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa32f-121">Header</span><span class="sxs-lookup"><span data-stu-id="fa32f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fa32f-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="fa32f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa32f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa32f-123">Library</span></span><br/> | <dl> <span data-ttu-id="fa32f-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa32f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa32f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fa32f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa32f-126">**IAMTimelineObj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fa32f-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




