---
description: Die RemoveAll-Methode entfernt dieses objektpermanent aus der Zeitachse, einschließlich untergeordneten Elementen und untergeordneten Elementen.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'Iamtimelineobj:: RemoveAll-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373899"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="d134f-103">Iamtimelineobj:: RemoveAll-Methode</span><span class="sxs-lookup"><span data-stu-id="d134f-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="d134f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d134f-104">\[Deprecated.</span></span> <span data-ttu-id="d134f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d134f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d134f-106">Die `RemoveAll` -Methode entfernt dieses objektpermanent aus der Zeitachse, einschließlich untergeordneten Elementen und untergeordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="d134f-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="d134f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d134f-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="d134f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d134f-108">Parameters</span></span>

<span data-ttu-id="d134f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d134f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d134f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d134f-110">Return value</span></span>

<span data-ttu-id="d134f-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d134f-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d134f-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d134f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d134f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d134f-113">Remarks</span></span>

<span data-ttu-id="d134f-114">Um ein Objekt zu entfernen, um es an anderer Stelle in der Zeitachse wiederherzustellen, nennen Sie [**iamtimelineobj:: Remove**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="d134f-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="d134f-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d134f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d134f-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d134f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d134f-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d134f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d134f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d134f-118">Requirements</span></span>



| <span data-ttu-id="d134f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d134f-119">Requirement</span></span> | <span data-ttu-id="d134f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d134f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d134f-121">Header</span><span class="sxs-lookup"><span data-stu-id="d134f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d134f-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d134f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d134f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d134f-123">Library</span></span><br/> | <dl> <span data-ttu-id="d134f-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d134f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d134f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d134f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d134f-126">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d134f-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d134f-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="d134f-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




