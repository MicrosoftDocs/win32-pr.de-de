---
description: Die getcutpoint-Methode ruft den Ausschneide Punkt ab.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Iamtimelinetrans:: getcutpoint-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361052"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="e6b2c-103">Iamtimelinetrans:: getcutpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="e6b2c-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="e6b2c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-104">\[Deprecated.</span></span> <span data-ttu-id="e6b2c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e6b2c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6b2c-106">Die- `GetCutPoint` Methode ruft den Ausschneide Punkt ab.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="e6b2c-107">Wenn Sie einen Übergang als Ausschneiden gerenden, ist der Ausschneide Punkt die Zeit, zu der der Übergang von einer Quelle zur nächsten übergeht.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="e6b2c-108">Standardmäßig ist dieser Wert die Mitte des Übergangs.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="e6b2c-109">Bei einem Übergang, der eine Sekunde umfasst, beträgt der Standard Ausschneide Punkt z. b. 0,5 Sekunden in den Übergang.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b2c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6b2c-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="e6b2c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b2c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b2c-112">*ptltime*</span><span class="sxs-lookup"><span data-stu-id="e6b2c-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b2c-113">Empfängt den Ausschneide Punkt in Bezug auf die Startzeit des Übergangs in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b2c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6b2c-114">Return value</span></span>

<span data-ttu-id="e6b2c-115">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="e6b2c-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e6b2c-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e6b2c-116">Return code</span></span>                                                                               | <span data-ttu-id="e6b2c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6b2c-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6b2c-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2c-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="e6b2c-119">Der Ausschneide Punkt wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-119">The cut point was not set.</span></span> <span data-ttu-id="e6b2c-120">Der zurückgegebene Wert ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="e6b2c-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2c-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e6b2c-122">Der Ausschneide Punkt wurde auf einen anderen Wert als den Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="e6b2c-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2c-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e6b2c-124">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="e6b2c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6b2c-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6b2c-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6b2c-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6b2c-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6b2c-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6b2c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6b2c-129">Requirements</span></span>



| <span data-ttu-id="e6b2c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6b2c-130">Requirement</span></span> | <span data-ttu-id="e6b2c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e6b2c-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b2c-132">Header</span><span class="sxs-lookup"><span data-stu-id="e6b2c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e6b2c-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2c-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6b2c-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e6b2c-134">Library</span></span><br/> | <dl> <span data-ttu-id="e6b2c-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e6b2c-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b2c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b2c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b2c-137">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e6b2c-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="e6b2c-138">**Iamtimelinetrans:: setcutpoint**</span><span class="sxs-lookup"><span data-stu-id="e6b2c-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="e6b2c-139">**Iamtimelinetrans:: getcutsonly**</span><span class="sxs-lookup"><span data-stu-id="e6b2c-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="e6b2c-140">**Iamtimeline:: transitionsenabled**</span><span class="sxs-lookup"><span data-stu-id="e6b2c-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="e6b2c-141">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e6b2c-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




