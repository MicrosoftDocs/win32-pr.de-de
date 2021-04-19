---
description: 'Die SetMediaTimes2-Methode legt die Start-und Startzeiten des Mediums fest. Diese Methode entspricht iamtimelinesrc:: setmediatimes, erfordert jedoch reftime-Werte.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Iamtimelinesrc:: SetMediaTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361487"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="ab780-104">Iamtimelinesrc:: SetMediaTimes2-Methode</span><span class="sxs-lookup"><span data-stu-id="ab780-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="ab780-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ab780-105">\[Deprecated.</span></span> <span data-ttu-id="ab780-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ab780-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ab780-107">Die `SetMediaTimes2` -Methode legt die Start-und Startzeiten des Mediums fest.</span><span class="sxs-lookup"><span data-stu-id="ab780-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="ab780-108">Diese Methode entspricht [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="ab780-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab780-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab780-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="ab780-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab780-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab780-111">*Starten*</span><span class="sxs-lookup"><span data-stu-id="ab780-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="ab780-112">Start Zeit der Medien in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ab780-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ab780-113">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="ab780-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="ab780-114">Die Endzeit des Mediums in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ab780-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab780-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab780-115">Return value</span></span>

<span data-ttu-id="ab780-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ab780-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab780-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab780-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab780-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab780-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ab780-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ab780-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ab780-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ab780-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ab780-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab780-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab780-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab780-122">Requirements</span></span>



| <span data-ttu-id="ab780-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab780-123">Requirement</span></span> | <span data-ttu-id="ab780-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ab780-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab780-125">Header</span><span class="sxs-lookup"><span data-stu-id="ab780-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ab780-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ab780-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab780-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab780-127">Library</span></span><br/> | <dl> <span data-ttu-id="ab780-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ab780-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab780-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab780-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab780-130">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ab780-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ab780-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ab780-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




