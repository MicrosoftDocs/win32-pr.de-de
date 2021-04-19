---
description: 'Mit der FixMediaTimes2-Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Diese Methode entspricht iamtimelinesrc:: fixmediatimes, erfordert jedoch reftime-Werte.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'Iamtimelinesrc:: FixMediaTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373577"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="7b9f4-104">Iamtimelinesrc:: FixMediaTimes2-Methode</span><span class="sxs-lookup"><span data-stu-id="7b9f4-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="7b9f4-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-105">\[Deprecated.</span></span> <span data-ttu-id="7b9f4-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7b9f4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b9f4-107">Mit der- `FixMediaTimes2` Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="7b9f4-108">Diese Methode entspricht [**iamtimelinesrc:: fixmediatimes**](iamtimelinesrc-fixmediatimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9f4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b9f4-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="7b9f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b9f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b9f4-111">*PStart*</span><span class="sxs-lookup"><span data-stu-id="7b9f4-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="7b9f4-112">Ein Zeiger auf eine Variable, die die Startzeit in Sekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="7b9f4-113">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="7b9f4-114">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="7b9f4-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="7b9f4-115">Ein Zeiger auf eine Variable, die die Endzeit in Sekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="7b9f4-116">Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b9f4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b9f4-117">Return value</span></span>

<span data-ttu-id="7b9f4-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b9f4-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b9f4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b9f4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b9f4-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b9f4-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7b9f4-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b9f4-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b9f4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b9f4-124">Requirements</span></span>



| <span data-ttu-id="7b9f4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b9f4-125">Requirement</span></span> | <span data-ttu-id="7b9f4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7b9f4-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9f4-127">Header</span><span class="sxs-lookup"><span data-stu-id="7b9f4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7b9f4-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7b9f4-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7b9f4-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b9f4-129">Library</span></span><br/> | <dl> <span data-ttu-id="7b9f4-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7b9f4-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9f4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b9f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9f4-132">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7b9f4-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7b9f4-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7b9f4-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




