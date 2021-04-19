---
description: 'Wird nicht unterstützt. Rufen Sie die iamtimeline:: kreateemptynode-Methode auf, um ein neues Timeline-Objekt zu erstellen. Nachdem ein Objekt erstellt wurde, können Sie den Typ nicht mehr ändern.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'Iamtimelineobj:: settimelinetype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367721"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="c6389-105">Iamtimelineobj:: settimelinetype-Methode</span><span class="sxs-lookup"><span data-stu-id="c6389-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="c6389-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6389-106">\[Deprecated.</span></span> <span data-ttu-id="c6389-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c6389-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c6389-108">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6389-108">Not supported.</span></span> <span data-ttu-id="c6389-109">Rufen Sie die [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) -Methode auf, um ein neues Timeline-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6389-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="c6389-110">Nachdem ein Objekt erstellt wurde, können Sie den Typ nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="c6389-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6389-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6389-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c6389-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6389-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6389-113">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="c6389-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c6389-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c6389-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6389-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6389-115">Return value</span></span>

<span data-ttu-id="c6389-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c6389-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6389-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6389-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6389-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6389-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6389-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c6389-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6389-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c6389-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c6389-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6389-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6389-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6389-122">Requirements</span></span>



| <span data-ttu-id="c6389-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6389-123">Requirement</span></span> | <span data-ttu-id="c6389-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c6389-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6389-125">Header</span><span class="sxs-lookup"><span data-stu-id="c6389-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c6389-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c6389-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c6389-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6389-127">Library</span></span><br/> | <dl> <span data-ttu-id="c6389-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c6389-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6389-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6389-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6389-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c6389-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




