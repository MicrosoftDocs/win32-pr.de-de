---
description: 'Mit der SetCutPoint2-Methode wird die Zeit festgelegt, zu der der Übergang von einer Quelle zum nächsten schneidet, wenn der Übergang als Ausschneiden gerendert wird. Diese Methode entspricht iamtimelinetrans:: setcutpoint, aber nimmt einen reftime-Wert an.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Iamtimelinetrans:: SetCutPoint2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371998"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="a80b9-104">Iamtimelinetrans:: SetCutPoint2-Methode</span><span class="sxs-lookup"><span data-stu-id="a80b9-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="a80b9-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a80b9-105">\[Deprecated.</span></span> <span data-ttu-id="a80b9-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a80b9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a80b9-107">Die- `SetCutPoint2` Methode legt die Zeit fest, zu der der Übergang von einer Quelle zum nächsten abbricht, wenn der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a80b9-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="a80b9-108">Diese Methode entspricht [**iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="a80b9-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80b9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a80b9-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="a80b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a80b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80b9-111">*Tltime*</span><span class="sxs-lookup"><span data-stu-id="a80b9-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a80b9-112">Der Ausschneide Punkt relativ zum Anfang des Übergangs in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a80b9-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a80b9-113">Return value</span></span>

<span data-ttu-id="a80b9-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a80b9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a80b9-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a80b9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a80b9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a80b9-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a80b9-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a80b9-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a80b9-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a80b9-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a80b9-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a80b9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a80b9-120">Requirements</span></span>



| <span data-ttu-id="a80b9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a80b9-121">Requirement</span></span> | <span data-ttu-id="a80b9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a80b9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a80b9-123">Header</span><span class="sxs-lookup"><span data-stu-id="a80b9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a80b9-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a80b9-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a80b9-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a80b9-125">Library</span></span><br/> | <dl> <span data-ttu-id="a80b9-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a80b9-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80b9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a80b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80b9-128">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a80b9-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="a80b9-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a80b9-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




