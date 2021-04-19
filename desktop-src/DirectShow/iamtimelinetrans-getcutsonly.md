---
description: Die getcutsonly-Methode bestimmt, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Iamtimelinetrans:: getcutsonly-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367189"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="1f641-104">Iamtimelinetrans:: getcutsonly-Methode</span><span class="sxs-lookup"><span data-stu-id="1f641-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="1f641-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1f641-105">\[Deprecated.</span></span> <span data-ttu-id="1f641-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1f641-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f641-107">Die- `GetCutsOnly` Methode bestimmt, ob der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="1f641-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="1f641-108">Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf.</span><span class="sxs-lookup"><span data-stu-id="1f641-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f641-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f641-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1f641-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f641-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f641-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="1f641-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1f641-112">Empfängt einen booleschen Wert, der angibt, ob der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="1f641-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="1f641-113">**True** gibt an, dass der Übergang eine sofortige Ausschneide ist.</span><span class="sxs-lookup"><span data-stu-id="1f641-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="1f641-114">Wenn der Wert **false** ist, tritt der Übergang über die normale Dauer auf.</span><span class="sxs-lookup"><span data-stu-id="1f641-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f641-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f641-115">Return value</span></span>

<span data-ttu-id="1f641-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f641-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f641-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f641-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f641-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f641-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f641-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1f641-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1f641-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1f641-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1f641-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f641-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f641-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f641-122">Requirements</span></span>



| <span data-ttu-id="1f641-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f641-123">Requirement</span></span> | <span data-ttu-id="1f641-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1f641-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f641-125">Header</span><span class="sxs-lookup"><span data-stu-id="1f641-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1f641-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1f641-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1f641-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f641-127">Library</span></span><br/> | <dl> <span data-ttu-id="1f641-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1f641-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f641-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f641-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f641-130">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1f641-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="1f641-131">**Iamtimelinetrans:: setcutsonly**</span><span class="sxs-lookup"><span data-stu-id="1f641-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="1f641-132">**Iamtimelinetrans:: getcutpoint**</span><span class="sxs-lookup"><span data-stu-id="1f641-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="1f641-133">**Iamtimeline:: transitionsenabled**</span><span class="sxs-lookup"><span data-stu-id="1f641-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="1f641-134">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="1f641-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




