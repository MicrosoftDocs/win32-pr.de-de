---
description: Die setgedämpf-Methode legt den gedämpften Zustand des Objekts fest. Ein mutobjekt wird nicht gerendert, aber es bleibt in der Zeitachse.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Iamtimelineobj:: setgedämpf-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361615"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="f6ede-104">Iamtimelineobj:: setgedämpf-Methode</span><span class="sxs-lookup"><span data-stu-id="f6ede-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="f6ede-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f6ede-105">\[Deprecated.</span></span> <span data-ttu-id="f6ede-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f6ede-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6ede-107">Die `SetMuted` -Methode legt den gedämpften Zustand des-Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="f6ede-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="f6ede-108">Ein mutobjekt wird nicht gerendert, aber es bleibt in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="f6ede-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ede-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6ede-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f6ede-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6ede-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ede-111">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="f6ede-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f6ede-112">Flag, das den Zustand "stumm" angibt.</span><span class="sxs-lookup"><span data-stu-id="f6ede-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="f6ede-113">**True** gibt an, dass das-Objekt und alle untergeordneten Elemente stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="f6ede-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ede-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6ede-114">Return value</span></span>

<span data-ttu-id="f6ede-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f6ede-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6ede-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6ede-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ede-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6ede-117">Remarks</span></span>

<span data-ttu-id="f6ede-118">Durch das Muting eines Objekts werden auch alle untergeordneten Elemente des-Objekts stumm.</span><span class="sxs-lookup"><span data-stu-id="f6ede-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="f6ede-119">Wenn Sie z. b. eine Spur stumm schalten, werden die Übergänge, Quellen und Effekte in dieser Spur ebenfalls stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="f6ede-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="f6ede-120">Wenn das Objekt nicht mehr stumm geschaltet wird, werden die untergeordneten Elemente in ihren vorherigen Zustand zurückversetzt, der möglicherweise stumm oder unstumm ist.</span><span class="sxs-lookup"><span data-stu-id="f6ede-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="f6ede-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f6ede-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6ede-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f6ede-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6ede-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6ede-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6ede-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6ede-124">Requirements</span></span>



| <span data-ttu-id="f6ede-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6ede-125">Requirement</span></span> | <span data-ttu-id="f6ede-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f6ede-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ede-127">Header</span><span class="sxs-lookup"><span data-stu-id="f6ede-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f6ede-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f6ede-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6ede-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6ede-129">Library</span></span><br/> | <dl> <span data-ttu-id="f6ede-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f6ede-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ede-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ede-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ede-132">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f6ede-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f6ede-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f6ede-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




