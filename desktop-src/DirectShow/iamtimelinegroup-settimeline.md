---
description: 'Wird nicht unterstützt. Stattdessen wird die iamtimeline:: addgroup-Methode aufgerufen.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'Iamtimelinegroup:: settimeline-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365738"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="05317-104">Iamtimelinegroup:: settimeline-Methode</span><span class="sxs-lookup"><span data-stu-id="05317-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="05317-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="05317-105">\[Deprecated.</span></span> <span data-ttu-id="05317-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="05317-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05317-107">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05317-107">Not supported.</span></span> <span data-ttu-id="05317-108">Stattdessen wird die [**iamtimeline:: addgroup**](iamtimeline-addgroup.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="05317-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="05317-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05317-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="05317-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05317-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05317-111">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="05317-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="05317-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="05317-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05317-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05317-113">Return value</span></span>

<span data-ttu-id="05317-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="05317-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05317-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05317-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05317-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05317-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05317-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="05317-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05317-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="05317-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05317-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05317-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05317-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05317-120">Requirements</span></span>



| <span data-ttu-id="05317-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05317-121">Requirement</span></span> | <span data-ttu-id="05317-122">Wert</span><span class="sxs-lookup"><span data-stu-id="05317-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05317-123">Header</span><span class="sxs-lookup"><span data-stu-id="05317-123">Header</span></span><br/>  | <dl> <span data-ttu-id="05317-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="05317-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05317-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05317-125">Library</span></span><br/> | <dl> <span data-ttu-id="05317-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="05317-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05317-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05317-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05317-128">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="05317-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




