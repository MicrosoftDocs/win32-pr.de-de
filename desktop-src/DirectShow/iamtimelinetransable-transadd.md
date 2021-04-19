---
description: Die transadd-Methode fügt dem-Objekt einen Übergang hinzu. Ein Objekt kann mehrere Übergänge aufweisen, aber Sie dürfen sich nicht rechtzeitig überlappen. Übergänge müssen innerhalb der Zeitbegrenzungen des-Objekts liegen.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Iamtimelinetransable:: transadd-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367820"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="47e06-105">Iamtimelinetransable:: transadd-Methode</span><span class="sxs-lookup"><span data-stu-id="47e06-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="47e06-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="47e06-106">\[Deprecated.</span></span> <span data-ttu-id="47e06-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="47e06-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="47e06-108">Die- `TransAdd` Methode fügt dem-Objekt einen Übergang hinzu.</span><span class="sxs-lookup"><span data-stu-id="47e06-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="47e06-109">Ein Objekt kann mehrere Übergänge aufweisen, aber Sie dürfen sich nicht rechtzeitig überlappen.</span><span class="sxs-lookup"><span data-stu-id="47e06-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="47e06-110">Übergänge müssen innerhalb der Zeitbegrenzungen des-Objekts liegen.</span><span class="sxs-lookup"><span data-stu-id="47e06-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e06-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="47e06-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="47e06-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e06-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e06-113">*ptrans*</span><span class="sxs-lookup"><span data-stu-id="47e06-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="47e06-114">Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des hinzu zufügenden Übergangs.</span><span class="sxs-lookup"><span data-stu-id="47e06-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e06-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47e06-115">Return value</span></span>

<span data-ttu-id="47e06-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="47e06-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="47e06-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="47e06-117">Return code</span></span>                                                                                   | <span data-ttu-id="47e06-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47e06-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="47e06-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47e06-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="47e06-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="47e06-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="47e06-122">Der Übergang kann nicht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="47e06-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="47e06-123"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="47e06-124">*ptrans* ist kein Zeiger auf einen Übergang.</span><span class="sxs-lookup"><span data-stu-id="47e06-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47e06-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47e06-125">Remarks</span></span>

<span data-ttu-id="47e06-126">Wenn der Übergang einen vorhandenen Übergang überlappt, gibt die Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="47e06-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="47e06-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="47e06-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="47e06-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="47e06-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="47e06-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47e06-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47e06-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47e06-130">Requirements</span></span>



| <span data-ttu-id="47e06-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47e06-131">Requirement</span></span> | <span data-ttu-id="47e06-132">Wert</span><span class="sxs-lookup"><span data-stu-id="47e06-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47e06-133">Header</span><span class="sxs-lookup"><span data-stu-id="47e06-133">Header</span></span><br/>  | <dl> <span data-ttu-id="47e06-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="47e06-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47e06-135">Library</span></span><br/> | <dl> <span data-ttu-id="47e06-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e06-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47e06-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e06-138">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="47e06-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="47e06-139">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="47e06-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




