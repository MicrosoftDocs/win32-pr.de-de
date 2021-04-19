---
description: Die getnexttrans-Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Iamtimelinetransable:: getnexttrans-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353419"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="1aa60-103">Iamtimelinetransable:: getnexttrans-Methode</span><span class="sxs-lookup"><span data-stu-id="1aa60-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="1aa60-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1aa60-104">\[Deprecated.</span></span> <span data-ttu-id="1aa60-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1aa60-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1aa60-106">Die- `GetNextTrans` Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa60-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa60-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aa60-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="1aa60-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aa60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa60-109">*pptrans* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1aa60-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa60-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs Objekts.</span><span class="sxs-lookup"><span data-stu-id="1aa60-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1aa60-111">*Pinout*</span><span class="sxs-lookup"><span data-stu-id="1aa60-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="1aa60-112">Ein Zeiger auf eine Variable, die die Zeit in 100-Nanosecond-Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="1aa60-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="1aa60-113">Bei der Eingabe gibt dieser Wert die Zeit an, nach der der Übergang gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aa60-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="1aa60-114">Bei der Ausgabe wird dieser Wert auf die Endzeit des Übergangs festgelegt, wenn ein Übergang abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1aa60-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa60-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aa60-115">Return value</span></span>

<span data-ttu-id="1aa60-116">Gibt s \_ OK zurück, wenn die Methode einen Übergang abruft, oder s \_ false, wenn kein Übergang gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1aa60-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="1aa60-117">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="1aa60-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa60-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa60-118">Remarks</span></span>

<span data-ttu-id="1aa60-119">Die Startzeit des Übergangs kann kleiner sein als die Zeit, die Sie in *Pinout* angegeben haben, wenn der Übergang die angegebene Zeitspanne überschreitet.</span><span class="sxs-lookup"><span data-stu-id="1aa60-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="1aa60-120">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="1aa60-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="1aa60-121">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="1aa60-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1aa60-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1aa60-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1aa60-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1aa60-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1aa60-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1aa60-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1aa60-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aa60-125">Requirements</span></span>



| <span data-ttu-id="1aa60-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aa60-126">Requirement</span></span> | <span data-ttu-id="1aa60-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1aa60-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa60-128">Header</span><span class="sxs-lookup"><span data-stu-id="1aa60-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1aa60-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1aa60-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1aa60-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1aa60-130">Library</span></span><br/> | <dl> <span data-ttu-id="1aa60-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1aa60-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa60-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aa60-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa60-133">**Iamtimelinetransable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1aa60-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="1aa60-134">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="1aa60-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




