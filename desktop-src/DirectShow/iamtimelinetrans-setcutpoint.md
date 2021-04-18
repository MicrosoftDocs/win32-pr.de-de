---
description: Mit der setcutpoint-Methode wird die Uhrzeit festgelegt, zu der der Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Iamtimelinetrans:: setcutpoint-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357649"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="a04e3-103">Iamtimelinetrans:: setcutpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="a04e3-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="a04e3-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a04e3-104">\[Deprecated.</span></span> <span data-ttu-id="a04e3-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a04e3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a04e3-106">Die- `SetCutPoint` Methode legt die Zeit fest, zu der der Übergang von einer Quelle zum nächsten abbricht, wenn der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a04e3-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a04e3-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="a04e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a04e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04e3-109">*Tltime*</span><span class="sxs-lookup"><span data-stu-id="a04e3-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a04e3-110">Der Ausschneide Punkt relativ zum Anfang des Übergangs in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="a04e3-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="a04e3-111">Wenn der Wert außerhalb der Grenzen des Übergangs liegt, wird er auf die nächste gültige Zeit abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a04e3-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04e3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a04e3-112">Return value</span></span>

<span data-ttu-id="a04e3-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a04e3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a04e3-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a04e3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04e3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a04e3-115">Remarks</span></span>

<span data-ttu-id="a04e3-116">Standardmäßig ist der Ausschneide Punkt die Mitte des Übergangs.</span><span class="sxs-lookup"><span data-stu-id="a04e3-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="a04e3-117">Bei einem Übergang, der eine Sekunde umfasst, beträgt der Standard Ausschneide Punkt z. b. 0,5 Sekunden in den Übergang.</span><span class="sxs-lookup"><span data-stu-id="a04e3-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="a04e3-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a04e3-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a04e3-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a04e3-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a04e3-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a04e3-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a04e3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a04e3-121">Requirements</span></span>



| <span data-ttu-id="a04e3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a04e3-122">Requirement</span></span> | <span data-ttu-id="a04e3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a04e3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a04e3-124">Header</span><span class="sxs-lookup"><span data-stu-id="a04e3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a04e3-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a04e3-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a04e3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a04e3-126">Library</span></span><br/> | <dl> <span data-ttu-id="a04e3-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a04e3-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04e3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a04e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04e3-129">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a04e3-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a04e3-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a04e3-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




