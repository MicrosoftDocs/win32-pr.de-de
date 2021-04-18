---
description: 'Mit der FixTimes2-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert. Diese Methode entspricht iamtimelineobj:: fixtimes, erfordert jedoch reftime-Werte.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Iamtimelineobj:: FixTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372762"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="70d4b-104">Iamtimelineobj:: FixTimes2-Methode</span><span class="sxs-lookup"><span data-stu-id="70d4b-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="70d4b-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="70d4b-105">\[Deprecated.</span></span> <span data-ttu-id="70d4b-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="70d4b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70d4b-107">`FixTimes2`Mit der-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="70d4b-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="70d4b-108">Diese Methode entspricht [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="70d4b-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d4b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="70d4b-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="70d4b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70d4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d4b-111">*PStart*</span><span class="sxs-lookup"><span data-stu-id="70d4b-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="70d4b-112">Ein Zeiger auf eine Variable, die die Startzeit in Sekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="70d4b-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="70d4b-113">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="70d4b-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="70d4b-114">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="70d4b-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="70d4b-115">Ein Zeiger auf eine Variable, die die Endzeit in Sekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="70d4b-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="70d4b-116">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="70d4b-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d4b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70d4b-117">Return value</span></span>

<span data-ttu-id="70d4b-118">Gibt \_ bei Erfolg S OK oder E \_ notintree zurück, wenn das Objekt nicht Teil einer Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="70d4b-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="70d4b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70d4b-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70d4b-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="70d4b-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70d4b-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="70d4b-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70d4b-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="70d4b-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70d4b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70d4b-123">Requirements</span></span>



| <span data-ttu-id="70d4b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70d4b-124">Requirement</span></span> | <span data-ttu-id="70d4b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="70d4b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70d4b-126">Header</span><span class="sxs-lookup"><span data-stu-id="70d4b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="70d4b-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="70d4b-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70d4b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70d4b-128">Library</span></span><br/> | <dl> <span data-ttu-id="70d4b-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="70d4b-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d4b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70d4b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d4b-131">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="70d4b-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="70d4b-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="70d4b-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




