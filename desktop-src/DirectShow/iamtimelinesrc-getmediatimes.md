---
description: Die getmediatimes-Methode ruft die Start-und Endzeit des Mediums ab.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Iamtimelinesrc:: getmediatimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372474"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="48aa2-103">Iamtimelinesrc:: getmediatimes-Methode</span><span class="sxs-lookup"><span data-stu-id="48aa2-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="48aa2-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="48aa2-104">\[Deprecated.</span></span> <span data-ttu-id="48aa2-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="48aa2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="48aa2-106">Die `GetMediaTimes` -Methode ruft die Start-und Endzeit des Mediums ab.</span><span class="sxs-lookup"><span data-stu-id="48aa2-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="48aa2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48aa2-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="48aa2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48aa2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48aa2-109">*PStart*</span><span class="sxs-lookup"><span data-stu-id="48aa2-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="48aa2-110">Empfängt die Start Zeit der Medien in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="48aa2-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="48aa2-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="48aa2-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="48aa2-112">Empfängt die Endzeit des Mediums in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="48aa2-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48aa2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48aa2-113">Return value</span></span>

<span data-ttu-id="48aa2-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="48aa2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48aa2-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48aa2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48aa2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48aa2-116">Remarks</span></span>

<span data-ttu-id="48aa2-117">Die Medien Zeiten sind relativ zur ursprünglichen Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="48aa2-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="48aa2-118">Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="48aa2-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="48aa2-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="48aa2-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="48aa2-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="48aa2-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="48aa2-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48aa2-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="48aa2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48aa2-122">Requirements</span></span>



| <span data-ttu-id="48aa2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48aa2-123">Requirement</span></span> | <span data-ttu-id="48aa2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="48aa2-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48aa2-125">Header</span><span class="sxs-lookup"><span data-stu-id="48aa2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="48aa2-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="48aa2-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="48aa2-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48aa2-127">Library</span></span><br/> | <dl> <span data-ttu-id="48aa2-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="48aa2-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48aa2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48aa2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48aa2-130">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48aa2-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="48aa2-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="48aa2-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




