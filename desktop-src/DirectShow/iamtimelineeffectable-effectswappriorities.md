---
description: Die effectionwappriority-Methode schaltet die Prioritäts Ebenen von zwei Effekten um.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Iamtimelineeffectable:: effectwapprioritäten-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365842"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="2e11f-103">Iamtimelineeffectable:: effeczwapprioritäten-Methode</span><span class="sxs-lookup"><span data-stu-id="2e11f-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="2e11f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2e11f-104">\[Deprecated.</span></span> <span data-ttu-id="2e11f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2e11f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e11f-106">Die- `EffectSwapPriorities` Methode schaltet die Prioritäts Ebenen von zwei Effekten um.</span><span class="sxs-lookup"><span data-stu-id="2e11f-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="2e11f-107">Bei zwei Prioritäts Werten vertauscht diese Methode die Auswirkungen auf diese Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="2e11f-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="2e11f-108">Wenn die-Methode zurückgegeben wird, liegt der Effekt, der sich auf der ersten Prioritätsstufe befand, auf der zweiten Prioritätsstufe und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="2e11f-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e11f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e11f-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="2e11f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e11f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e11f-111">*Prioritya*</span><span class="sxs-lookup"><span data-stu-id="2e11f-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="2e11f-112">Die erste Prioritätsstufe, bei der die Effekte ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e11f-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="2e11f-113">*Priorityb*</span><span class="sxs-lookup"><span data-stu-id="2e11f-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="2e11f-114">Die zweite Prioritätsstufe, bei der die Effekte ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e11f-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e11f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e11f-115">Return value</span></span>

<span data-ttu-id="2e11f-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e11f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e11f-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e11f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e11f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e11f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e11f-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2e11f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e11f-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="2e11f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e11f-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2e11f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e11f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e11f-122">Requirements</span></span>



| <span data-ttu-id="2e11f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e11f-123">Requirement</span></span> | <span data-ttu-id="2e11f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2e11f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e11f-125">Header</span><span class="sxs-lookup"><span data-stu-id="2e11f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e11f-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2e11f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e11f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e11f-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e11f-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="2e11f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e11f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e11f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e11f-130">**Iamtimelineeffectable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2e11f-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="2e11f-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="2e11f-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




