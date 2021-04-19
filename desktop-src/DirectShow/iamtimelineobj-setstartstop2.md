---
description: 'Mit der SetStartStop2-Methode werden die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts festgelegt. Diese Methode entspricht iamtimelineobj:: setstartstation, erfordert jedoch reftime-Werte.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Iamtimelineobj:: SetStartStop2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356001"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="4c252-104">Iamtimelineobj:: SetStartStop2-Methode</span><span class="sxs-lookup"><span data-stu-id="4c252-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="4c252-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4c252-105">\[Deprecated.</span></span> <span data-ttu-id="4c252-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4c252-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c252-107">Die `SetStartStop2` -Methode legt die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="4c252-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="4c252-108">Diese Methode entspricht [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="4c252-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c252-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c252-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4c252-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c252-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c252-111">*Starten*</span><span class="sxs-lookup"><span data-stu-id="4c252-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="4c252-112">Die neue Startzeit in Sekunden oder – 1, um die vorhandene Startzeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4c252-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="4c252-113">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="4c252-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4c252-114">Neue Endzeit, in Sekunden oder – 1, um die vorhandene Endzeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4c252-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c252-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c252-115">Return value</span></span>

<span data-ttu-id="4c252-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="4c252-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4c252-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4c252-117">Return code</span></span>                                                                                  | <span data-ttu-id="4c252-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c252-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="4c252-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c252-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4c252-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4c252-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="4c252-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4c252-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4c252-122">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="4c252-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="4c252-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4c252-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="4c252-124">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4c252-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="4c252-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c252-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c252-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4c252-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c252-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4c252-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c252-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c252-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c252-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c252-129">Requirements</span></span>



| <span data-ttu-id="4c252-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c252-130">Requirement</span></span> | <span data-ttu-id="4c252-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4c252-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c252-132">Header</span><span class="sxs-lookup"><span data-stu-id="4c252-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4c252-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4c252-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c252-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c252-134">Library</span></span><br/> | <dl> <span data-ttu-id="4c252-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4c252-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c252-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c252-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c252-137">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4c252-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4c252-138">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="4c252-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




