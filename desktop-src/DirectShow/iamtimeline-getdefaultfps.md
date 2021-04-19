---
description: 'Die getdefaultfps-Methode ruft die Standardausgabe Frame Rate in Frames pro Sekunde (fps) ab. Gruppen verwenden diesen Wert als Standard Frame Rate. Um die Framerate einer Gruppe festzulegen, müssen Sie die iamtimelinegroup:: setoutputfps-Methode für die Gruppe aufrufen.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Iamtimeline:: getdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358373"
---
# <a name="iamtimelinegetdefaultfps-method"></a><span data-ttu-id="a56db-105">Iamtimeline:: getdefaultfps-Methode</span><span class="sxs-lookup"><span data-stu-id="a56db-105">IAMTimeline::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="a56db-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a56db-106">\[Deprecated.</span></span> <span data-ttu-id="a56db-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a56db-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a56db-108">Die- `GetDefaultFPS` Methode ruft die Standardausgabe Frame Rate in Frames pro Sekunde (fps) ab.</span><span class="sxs-lookup"><span data-stu-id="a56db-108">The `GetDefaultFPS` method retrieves the default output frame rate, in frames per second (FPS).</span></span> <span data-ttu-id="a56db-109">Gruppen verwenden diesen Wert als Standard Frame Rate.</span><span class="sxs-lookup"><span data-stu-id="a56db-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="a56db-110">Um die Framerate einer Gruppe festzulegen, müssen Sie die [**iamtimelinegroup:: setoutputfps**](iamtimelinegroup-setoutputfps.md) -Methode für die Gruppe aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a56db-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56db-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a56db-111">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="a56db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56db-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56db-113">*pfps*</span><span class="sxs-lookup"><span data-stu-id="a56db-113">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="a56db-114">Empfängt die Standardbildrate in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="a56db-114">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56db-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a56db-115">Return value</span></span>

<span data-ttu-id="a56db-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a56db-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a56db-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a56db-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56db-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a56db-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a56db-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a56db-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a56db-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a56db-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a56db-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a56db-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a56db-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a56db-122">Requirements</span></span>



| <span data-ttu-id="a56db-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a56db-123">Requirement</span></span> | <span data-ttu-id="a56db-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a56db-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a56db-125">Header</span><span class="sxs-lookup"><span data-stu-id="a56db-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a56db-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a56db-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a56db-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a56db-127">Library</span></span><br/> | <dl> <span data-ttu-id="a56db-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a56db-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a56db-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a56db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56db-130">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a56db-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="a56db-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a56db-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




