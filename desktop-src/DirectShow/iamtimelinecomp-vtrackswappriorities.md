---
description: Die vtracktauappriority-Methode schaltet die Prioritätsstufen von zwei nach Titeln um.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Iamtimelinecomp:: vtracktauapprioritäten-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354840"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="d66b0-103">Iamtimelinecomp:: vtracktauapprioritäten-Methode</span><span class="sxs-lookup"><span data-stu-id="d66b0-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="d66b0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d66b0-104">\[Deprecated.</span></span> <span data-ttu-id="d66b0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d66b0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d66b0-106">Die- `VTrackSwapPriorities` Methode schaltet die Prioritäts Ebenen von zwei-Spuren um.</span><span class="sxs-lookup"><span data-stu-id="d66b0-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="d66b0-107">Bei zwei Prioritätsstufen schaltet diese Methode die virtuellen Spuren in diese Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="d66b0-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="d66b0-108">Wenn die-Methode zurückgibt, befindet sich der Titel, der sich auf der ersten Prioritäts Ebene befand, jetzt auf der zweiten Prioritätsstufe (und umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="d66b0-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d66b0-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="d66b0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d66b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66b0-111">*Virtualtracka*</span><span class="sxs-lookup"><span data-stu-id="d66b0-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="d66b0-112">Die erste Prioritätsstufe, bei der virtuelle Spuren ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d66b0-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="d66b0-113">*Virtualtrackb*</span><span class="sxs-lookup"><span data-stu-id="d66b0-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="d66b0-114">Die zweite Prioritätsstufe, bei der virtuelle Spuren ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d66b0-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66b0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d66b0-115">Return value</span></span>

<span data-ttu-id="d66b0-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d66b0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d66b0-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d66b0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66b0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d66b0-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d66b0-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d66b0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d66b0-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d66b0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d66b0-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d66b0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d66b0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d66b0-122">Requirements</span></span>



| <span data-ttu-id="d66b0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d66b0-123">Requirement</span></span> | <span data-ttu-id="d66b0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d66b0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d66b0-125">Header</span><span class="sxs-lookup"><span data-stu-id="d66b0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d66b0-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d66b0-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d66b0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d66b0-127">Library</span></span><br/> | <dl> <span data-ttu-id="d66b0-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d66b0-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66b0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d66b0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66b0-130">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d66b0-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="d66b0-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="d66b0-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




