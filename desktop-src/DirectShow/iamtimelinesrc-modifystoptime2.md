---
description: 'Die ModifyStopTime2-Methode legt die Endzeit fest. Diese Methode entspricht iamtimelinesrc:: modifystoptime, aber nimmt einen reftime-Wert an.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Iamtimelinesrc:: ModifyStopTime2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370819"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="7a7e6-104">Iamtimelinesrc:: ModifyStopTime2-Methode</span><span class="sxs-lookup"><span data-stu-id="7a7e6-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="7a7e6-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-105">\[Deprecated.</span></span> <span data-ttu-id="7a7e6-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7a7e6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7a7e6-107">Die- `ModifyStopTime2` Methode legt die Endzeit fest.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="7a7e6-108">Diese Methode entspricht [**iamtimelinesrc:: modifystoptime**](iamtimelinesrc-modifystoptime.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a7e6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a7e6-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="7a7e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a7e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a7e6-111">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="7a7e6-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="7a7e6-112">Neue Endzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a7e6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a7e6-113">Return value</span></span>

<span data-ttu-id="7a7e6-114">Gibt \_ bei Erfolg S OK oder E \_ invalidArg zurück, wenn die angegebene Zeit nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7e6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a7e6-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7a7e6-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7a7e6-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7a7e6-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a7e6-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a7e6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a7e6-119">Requirements</span></span>



| <span data-ttu-id="7a7e6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a7e6-120">Requirement</span></span> | <span data-ttu-id="7a7e6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7a7e6-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7e6-122">Header</span><span class="sxs-lookup"><span data-stu-id="7a7e6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7a7e6-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7a7e6-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7a7e6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a7e6-124">Library</span></span><br/> | <dl> <span data-ttu-id="7a7e6-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7a7e6-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a7e6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a7e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7e6-127">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7a7e6-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7a7e6-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7a7e6-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




