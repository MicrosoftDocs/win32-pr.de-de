---
description: 'Die setsubobjectguidb-Methode gibt die GUID des untergeordneten Objekts an, das diesem Objekt zugeordnet ist. Diese Methode entspricht iamtimelineobj:: setsubobjectguid, nimmt aber einen BSTR-Wert an.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'Iamtimelineobj:: setsubobjectguidb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373747"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="d9ca4-104">Iamtimelineobj:: setsubobjectguidb-Methode</span><span class="sxs-lookup"><span data-stu-id="d9ca4-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="d9ca4-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-105">\[Deprecated.</span></span> <span data-ttu-id="d9ca4-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d9ca4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9ca4-107">Die- `SetSubObjectGUIDB` Methode gibt die GUID des untergeordneten Objekts an, das diesem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="d9ca4-108">Diese Methode entspricht [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) , nimmt aber einen **BSTR** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ca4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9ca4-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d9ca4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9ca4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ca4-111">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="d9ca4-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d9ca4-112">**BSTR** , das die GUID des unter Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ca4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9ca4-113">Return value</span></span>

<span data-ttu-id="d9ca4-114">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9ca4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9ca4-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9ca4-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d9ca4-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d9ca4-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ca4-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9ca4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9ca4-119">Requirements</span></span>



| <span data-ttu-id="d9ca4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9ca4-120">Requirement</span></span> | <span data-ttu-id="d9ca4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9ca4-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ca4-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9ca4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9ca4-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d9ca4-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d9ca4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9ca4-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9ca4-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d9ca4-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ca4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9ca4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ca4-127">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d9ca4-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d9ca4-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="d9ca4-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




