---
description: 'Die GetMediaTimes2-Methode ruft die Start-und Endzeit des Mediums ab. Diese Methode entspricht iamtimelinesrc:: getmediatimes, erfordert jedoch reftime-Werte.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'Iamtimelinesrc:: GetMediaTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362008"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="d6cd4-104">Iamtimelinesrc:: GetMediaTimes2-Methode</span><span class="sxs-lookup"><span data-stu-id="d6cd4-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="d6cd4-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-105">\[Deprecated.</span></span> <span data-ttu-id="d6cd4-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d6cd4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d6cd4-107">Die `GetMediaTimes2` -Methode ruft die Start-und Endzeit des Mediums ab.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="d6cd4-108">Diese Methode entspricht [**iamtimelinesrc:: getmediatimes**](iamtimelinesrc-getmediatimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6cd4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6cd4-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d6cd4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6cd4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6cd4-111">*PStart*</span><span class="sxs-lookup"><span data-stu-id="d6cd4-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d6cd4-112">Empfängt die Start Zeit des Mediums in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d6cd4-113">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="d6cd4-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d6cd4-114">Empfängt die Endzeit des Mediums in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6cd4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6cd4-115">Return value</span></span>

<span data-ttu-id="d6cd4-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6cd4-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6cd4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6cd4-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6cd4-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6cd4-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d6cd4-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6cd4-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6cd4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6cd4-122">Requirements</span></span>



| <span data-ttu-id="d6cd4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6cd4-123">Requirement</span></span> | <span data-ttu-id="d6cd4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d6cd4-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6cd4-125">Header</span><span class="sxs-lookup"><span data-stu-id="d6cd4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d6cd4-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d6cd4-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d6cd4-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6cd4-127">Library</span></span><br/> | <dl> <span data-ttu-id="d6cd4-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d6cd4-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6cd4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6cd4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cd4-130">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d6cd4-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d6cd4-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="d6cd4-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




