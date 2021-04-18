---
description: Die vtrackgetcount-Methode ruft die Anzahl der in der Komposition enthaltenen virtuellen Spuren ab.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'Iamtimelinecomp:: vtrackgetcount-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372698"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="e7663-103">Iamtimelinecomp:: vtrackgetcount-Methode</span><span class="sxs-lookup"><span data-stu-id="e7663-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="e7663-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e7663-104">\[Deprecated.</span></span> <span data-ttu-id="e7663-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e7663-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7663-106">Die- `VTrackGetCount` Methode ruft die Anzahl der in der Komposition enthaltenen virtuellen Spuren ab.</span><span class="sxs-lookup"><span data-stu-id="e7663-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7663-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7663-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e7663-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7663-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7663-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e7663-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e7663-110">Empfängt die Anzahl der virtuellen Spuren.</span><span class="sxs-lookup"><span data-stu-id="e7663-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7663-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7663-111">Return value</span></span>

<span data-ttu-id="e7663-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e7663-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7663-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7663-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7663-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7663-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7663-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e7663-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7663-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e7663-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7663-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7663-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7663-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7663-118">Requirements</span></span>



| <span data-ttu-id="e7663-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7663-119">Requirement</span></span> | <span data-ttu-id="e7663-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e7663-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7663-121">Header</span><span class="sxs-lookup"><span data-stu-id="e7663-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e7663-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e7663-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7663-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7663-123">Library</span></span><br/> | <dl> <span data-ttu-id="e7663-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e7663-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7663-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7663-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7663-126">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7663-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="e7663-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e7663-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




