---
description: Mit der fixtimes-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Iamtimelineobj:: fixtimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362172"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="cc939-103">Iamtimelineobj:: fixtimes-Methode</span><span class="sxs-lookup"><span data-stu-id="cc939-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="cc939-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cc939-104">\[Deprecated.</span></span> <span data-ttu-id="cc939-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cc939-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc939-106">`FixTimes`Mit der-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="cc939-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc939-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc939-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="cc939-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc939-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc939-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="cc939-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="cc939-110">Zeiger auf eine Variable, die die Startzeit in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="cc939-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="cc939-111">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc939-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="cc939-112">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="cc939-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="cc939-113">Ein Zeiger auf eine Variable, die die Endzeit in 100-Nanosecond-Einheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="cc939-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="cc939-114">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc939-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc939-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc939-115">Return value</span></span>

<span data-ttu-id="cc939-116">Gibt \_ bei Erfolg S OK oder E \_ notintree zurück, wenn das Objekt nicht Teil einer Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="cc939-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc939-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc939-117">Remarks</span></span>

<span data-ttu-id="cc939-118">Während des Renderings rundet der die Start-und Endzeit des Objekts auf die nächste Frame Grenze.</span><span class="sxs-lookup"><span data-stu-id="cc939-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="cc939-119">Allerdings werden die Zeiten des Objekts von der nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc939-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="cc939-120">Wenn Sie die Gruppen Frame Rate ändern, werden die gerundeten Zeiten immer aus den ursprünglichen Zeiten berechnet.</span><span class="sxs-lookup"><span data-stu-id="cc939-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="cc939-121">Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="cc939-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="cc939-122">Verwenden Sie diese Methode, um genaue Start-und Endzeit im gerenderten Projekt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="cc939-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="cc939-123">Sie sollten z. b. die gerundeten Zeiten statt der ursprünglichen Start-und Endzeit des Objekts suchen.</span><span class="sxs-lookup"><span data-stu-id="cc939-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="cc939-124">Rufen Sie [**iamtimelineobj:: getstarthalte**](iamtimelineobj-getstartstop.md) auf, um die ursprünglichen Zeiten abzurufen, und übergeben Sie diese Werte an `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="cc939-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="cc939-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cc939-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc939-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cc939-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc939-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc939-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc939-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc939-128">Requirements</span></span>



| <span data-ttu-id="cc939-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc939-129">Requirement</span></span> | <span data-ttu-id="cc939-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cc939-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc939-131">Header</span><span class="sxs-lookup"><span data-stu-id="cc939-131">Header</span></span><br/>  | <dl> <span data-ttu-id="cc939-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cc939-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc939-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc939-133">Library</span></span><br/> | <dl> <span data-ttu-id="cc939-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cc939-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc939-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc939-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc939-136">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cc939-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="cc939-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cc939-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




