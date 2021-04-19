---
description: Die trackgetpriority-Methode ruft die Prioritäts Ebene des-Objekts ab.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Iamtimelinevirtualtrack:: trackgetpriority-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359767"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="e5b5f-103">Iamtimelinevirtualtrack:: trackgetpriority-Methode</span><span class="sxs-lookup"><span data-stu-id="e5b5f-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="e5b5f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-104">\[Deprecated.</span></span> <span data-ttu-id="e5b5f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e5b5f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5b5f-106">Die `TrackGetPriority` -Methode ruft die Prioritäts Ebene des-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b5f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5b5f-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="e5b5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5b5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b5f-109">*ppriority*</span><span class="sxs-lookup"><span data-stu-id="e5b5f-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b5f-110">Ein Zeiger auf eine Variable, die die Prioritäts Ebene empfängt.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="e5b5f-111">Wenn das Objekt nicht Teil einer Zeitachse ist, wird der Wert auf – 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b5f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5b5f-112">Return value</span></span>

<span data-ttu-id="e5b5f-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5b5f-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b5f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5b5f-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5b5f-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5b5f-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e5b5f-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5b5f-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5b5f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5b5f-119">Requirements</span></span>



| <span data-ttu-id="e5b5f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5b5f-120">Requirement</span></span> | <span data-ttu-id="e5b5f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e5b5f-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b5f-122">Header</span><span class="sxs-lookup"><span data-stu-id="e5b5f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e5b5f-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e5b5f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5b5f-124">Library</span></span><br/> | <dl> <span data-ttu-id="e5b5f-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5f-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b5f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5b5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b5f-127">**Iamtimelinevirtualtrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e5b5f-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="e5b5f-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e5b5f-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




