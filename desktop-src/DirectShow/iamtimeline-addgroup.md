---
description: Die addgroup-Methode fügt der Zeitachse eine Gruppe hinzu.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Iamtimeline:: addgroup-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358344"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="cf85f-103">Iamtimeline:: addgroup-Methode</span><span class="sxs-lookup"><span data-stu-id="cf85f-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="cf85f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cf85f-104">\[Deprecated.</span></span> <span data-ttu-id="cf85f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cf85f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf85f-106">Die- `AddGroup` Methode fügt der Zeitachse eine Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="cf85f-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf85f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf85f-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="cf85f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf85f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf85f-109">*pgroup*</span><span class="sxs-lookup"><span data-stu-id="cf85f-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="cf85f-110">Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cf85f-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf85f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf85f-111">Return value</span></span>

<span data-ttu-id="cf85f-112">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="cf85f-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cf85f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cf85f-113">Return code</span></span>                                                                                   | <span data-ttu-id="cf85f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf85f-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="cf85f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf85f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf85f-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cf85f-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="cf85f-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cf85f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cf85f-118">Die maximale Anzahl von Gruppen wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="cf85f-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="cf85f-119"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="cf85f-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="cf85f-120">Das Objekt ist keine Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cf85f-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="cf85f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf85f-121">Remarks</span></span>

<span data-ttu-id="cf85f-122">Derzeit unterstützen Zeitachsen maximal 32 Gruppen.</span><span class="sxs-lookup"><span data-stu-id="cf85f-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="cf85f-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cf85f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf85f-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cf85f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf85f-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf85f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf85f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf85f-126">Requirements</span></span>



| <span data-ttu-id="cf85f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf85f-127">Requirement</span></span> | <span data-ttu-id="cf85f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cf85f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf85f-129">Header</span><span class="sxs-lookup"><span data-stu-id="cf85f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cf85f-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cf85f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf85f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf85f-131">Library</span></span><br/> | <dl> <span data-ttu-id="cf85f-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cf85f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf85f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf85f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf85f-134">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cf85f-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="cf85f-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cf85f-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




