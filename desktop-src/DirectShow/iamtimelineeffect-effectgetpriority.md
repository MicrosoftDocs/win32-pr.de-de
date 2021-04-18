---
description: Die effectgetpriority-Methode ruft die Prioritäts Ebene des Effekts ab. Für ein bestimmtes Objekt wendet die Renderingengine Effekte in der Reihenfolge ihrer Priorität an, beginnend mit der Prioritätsstufe 0.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Iamtimelineeffect:: effectgetpriority-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371568"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="cc965-104">Iamtimelineeffect:: effectgetpriority-Methode</span><span class="sxs-lookup"><span data-stu-id="cc965-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="cc965-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cc965-105">\[Deprecated.</span></span> <span data-ttu-id="cc965-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cc965-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc965-107">Die `EffectGetPriority` -Methode ruft die Prioritäts Ebene des Effekts ab.</span><span class="sxs-lookup"><span data-stu-id="cc965-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="cc965-108">Für ein bestimmtes Objekt wendet die Renderingengine Effekte in der Reihenfolge ihrer Priorität an, beginnend mit der Prioritätsstufe 0.</span><span class="sxs-lookup"><span data-stu-id="cc965-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc965-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc965-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cc965-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc965-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc965-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="cc965-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="cc965-112">Empfängt die Prioritätsstufe.</span><span class="sxs-lookup"><span data-stu-id="cc965-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc965-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc965-113">Return value</span></span>

<span data-ttu-id="cc965-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cc965-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc965-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc965-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc965-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc965-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc965-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cc965-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc965-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cc965-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc965-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc965-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc965-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc965-120">Requirements</span></span>



| <span data-ttu-id="cc965-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc965-121">Requirement</span></span> | <span data-ttu-id="cc965-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cc965-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc965-123">Header</span><span class="sxs-lookup"><span data-stu-id="cc965-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cc965-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cc965-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc965-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc965-125">Library</span></span><br/> | <dl> <span data-ttu-id="cc965-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cc965-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc965-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc965-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc965-128">**Iamtimelineeffect-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cc965-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="cc965-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cc965-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




