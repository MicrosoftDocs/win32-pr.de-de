---
description: 'Die GetCutPoint2-Methode ruft den Ausschneide Punkt ab. Diese Methode entspricht iamtimelinetrans:: getcutpoint, aber nimmt einen reftime-Wert an.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'Iamtimelinetrans:: GetCutPoint2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371554"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="0a431-104">Iamtimelinetrans:: GetCutPoint2-Methode</span><span class="sxs-lookup"><span data-stu-id="0a431-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="0a431-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0a431-105">\[Deprecated.</span></span> <span data-ttu-id="0a431-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0a431-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a431-107">Die- `GetCutPoint2` Methode ruft den Ausschneide Punkt ab.</span><span class="sxs-lookup"><span data-stu-id="0a431-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="0a431-108">Diese Methode entspricht [**iamtimelinetrans:: getcutpoint**](iamtimelinetrans-getcutpoint.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="0a431-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a431-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a431-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="0a431-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a431-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a431-111">*ptltime*</span><span class="sxs-lookup"><span data-stu-id="0a431-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0a431-112">Empfängt den Ausschneide Punkt relativ zur Startzeit des Übergangs in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0a431-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a431-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a431-113">Return value</span></span>

<span data-ttu-id="0a431-114">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="0a431-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="0a431-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a431-115">Return code</span></span>                                                                               | <span data-ttu-id="0a431-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a431-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a431-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0a431-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="0a431-118">Der Ausschneide Punkt wurde nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0a431-118">The cut point was not set.</span></span> <span data-ttu-id="0a431-119">Der zurückgegebene Wert ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="0a431-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="0a431-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a431-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0a431-121">Der Ausschneide Punkt wurde auf einen anderen Wert als den Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0a431-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="0a431-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0a431-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0a431-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="0a431-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="0a431-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a431-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a431-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0a431-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a431-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0a431-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a431-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a431-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a431-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a431-128">Requirements</span></span>



| <span data-ttu-id="0a431-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a431-129">Requirement</span></span> | <span data-ttu-id="0a431-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0a431-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a431-131">Header</span><span class="sxs-lookup"><span data-stu-id="0a431-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0a431-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0a431-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a431-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a431-133">Library</span></span><br/> | <dl> <span data-ttu-id="0a431-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0a431-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a431-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a431-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a431-136">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a431-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="0a431-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="0a431-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




