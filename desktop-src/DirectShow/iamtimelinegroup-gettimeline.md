---
description: Die getTimeline-Methode ruft die Zeitachse ab, zu der diese Gruppe gehört.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'Iamtimelinegroup:: getTimeline-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371133"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="638a9-103">Iamtimelinegroup:: getTimeline-Methode</span><span class="sxs-lookup"><span data-stu-id="638a9-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="638a9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="638a9-104">\[Deprecated.</span></span> <span data-ttu-id="638a9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="638a9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="638a9-106">Die- `GetTimeline` Methode ruft die Zeitachse ab, zu der diese Gruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="638a9-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="638a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="638a9-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="638a9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="638a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="638a9-109">*pptimeline* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="638a9-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="638a9-110">Empfängt die [**iamtimeline**](iamtimeline.md) -Schnittstelle der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="638a9-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="638a9-111">Wenn die Gruppe nicht Teil einer Zeitachse ist, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="638a9-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="638a9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="638a9-112">Return value</span></span>

<span data-ttu-id="638a9-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="638a9-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="638a9-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="638a9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="638a9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="638a9-115">Remarks</span></span>

<span data-ttu-id="638a9-116">Wenn der in *pptimeline* zurückgegebene Wert nicht **null** ist, weist die **iamtimeline** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="638a9-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="638a9-117">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="638a9-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="638a9-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="638a9-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="638a9-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="638a9-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="638a9-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="638a9-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="638a9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="638a9-121">Requirements</span></span>



| <span data-ttu-id="638a9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="638a9-122">Requirement</span></span> | <span data-ttu-id="638a9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="638a9-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="638a9-124">Header</span><span class="sxs-lookup"><span data-stu-id="638a9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="638a9-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="638a9-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="638a9-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="638a9-126">Library</span></span><br/> | <dl> <span data-ttu-id="638a9-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="638a9-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638a9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="638a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638a9-129">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="638a9-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="638a9-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="638a9-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




