---
description: Mit der clearallgroups-Methode werden alle Gruppen aus der Zeitachse zusammen mit allen in diesen Gruppen enthaltenen Objekten entfernt.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'Iamtimeline:: clearallgroups-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354108"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="e2df9-103">Iamtimeline:: clearallgroups-Methode</span><span class="sxs-lookup"><span data-stu-id="e2df9-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="e2df9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e2df9-104">\[Deprecated.</span></span> <span data-ttu-id="e2df9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e2df9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e2df9-106">Die- `ClearAllGroups` Methode entfernt alle Gruppen aus der Zeitachse zusammen mit allen in diesen Gruppen enthaltenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="e2df9-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2df9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2df9-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="e2df9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2df9-108">Parameters</span></span>

<span data-ttu-id="e2df9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e2df9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2df9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2df9-110">Return value</span></span>

<span data-ttu-id="e2df9-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2df9-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e2df9-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2df9-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2df9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2df9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2df9-114">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e2df9-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2df9-115">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e2df9-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2df9-116">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2df9-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2df9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2df9-117">Requirements</span></span>



| <span data-ttu-id="e2df9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2df9-118">Requirement</span></span> | <span data-ttu-id="e2df9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2df9-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2df9-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2df9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2df9-121"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e2df9-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e2df9-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2df9-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2df9-123"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e2df9-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2df9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2df9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2df9-125">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2df9-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e2df9-126">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e2df9-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




