---
description: 'Die SplitAt2-Methode teilt das Objekt zum angegebenen Zeitpunkt. Diese Methode entspricht iamtimelinesplitting:: splitat, aber nimmt einen reftime-Wert an.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Iamtimelinesplicustom:: SplitAt2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358278"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="440ae-104">Iamtimelinesplicustom:: SplitAt2-Methode</span><span class="sxs-lookup"><span data-stu-id="440ae-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="440ae-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="440ae-105">\[Deprecated.</span></span> <span data-ttu-id="440ae-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="440ae-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="440ae-107">Die- `SplitAt2` Methode teilt das Objekt zum angegebenen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="440ae-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="440ae-108">Diese Methode entspricht [**iamtimelinesplitting:: splitat**](iamtimelinesplittable-splitat.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.</span><span class="sxs-lookup"><span data-stu-id="440ae-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="440ae-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="440ae-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="440ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="440ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440ae-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="440ae-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="440ae-112">Der Zeitpunkt, an dem das Objekt in Relation zum Anfang der Zeitachse geteilt werden soll (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="440ae-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="440ae-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="440ae-113">Return value</span></span>

<span data-ttu-id="440ae-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="440ae-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="440ae-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="440ae-115">Possible values include the following:</span></span>



| <span data-ttu-id="440ae-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="440ae-116">Return code</span></span>                                                                                   | <span data-ttu-id="440ae-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="440ae-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="440ae-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="440ae-119">Nichts zu teilen.</span><span class="sxs-lookup"><span data-stu-id="440ae-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="440ae-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="440ae-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="440ae-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="440ae-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="440ae-123">Das Objekt ist zu diesem Zeitpunkt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="440ae-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="440ae-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="440ae-125">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="440ae-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="440ae-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="440ae-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="440ae-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="440ae-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="440ae-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="440ae-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="440ae-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="440ae-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="440ae-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="440ae-130">Requirements</span></span>



| <span data-ttu-id="440ae-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="440ae-131">Requirement</span></span> | <span data-ttu-id="440ae-132">Wert</span><span class="sxs-lookup"><span data-stu-id="440ae-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="440ae-133">Header</span><span class="sxs-lookup"><span data-stu-id="440ae-133">Header</span></span><br/>  | <dl> <span data-ttu-id="440ae-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="440ae-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="440ae-135">Library</span></span><br/> | <dl> <span data-ttu-id="440ae-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="440ae-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="440ae-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="440ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440ae-138">**Iamtimelinesplicustom-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="440ae-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="440ae-139">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="440ae-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




