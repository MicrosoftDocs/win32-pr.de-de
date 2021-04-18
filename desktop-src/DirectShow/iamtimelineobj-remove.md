---
description: Die Remove-Methode entfernt dieses Objekt aus der Zeitachse (einschließlich untergeordneter Objekte, aber nicht untergeordneter Elemente) für die erneute initizierung an anderer Stelle.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Iamtimelineobj:: Remove-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360955"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="30742-103">Iamtimelineobj:: Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="30742-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="30742-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="30742-104">\[Deprecated.</span></span> <span data-ttu-id="30742-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="30742-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30742-106">Die- `Remove` Methode entfernt dieses-Objekt aus der Zeitachse (einschließlich untergeordneter Objekte, aber nicht untergeordneter Elemente) für die Wiederherstellung an anderer Stelle.</span><span class="sxs-lookup"><span data-stu-id="30742-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="30742-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30742-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="30742-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30742-108">Parameters</span></span>

<span data-ttu-id="30742-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="30742-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30742-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30742-110">Return value</span></span>

<span data-ttu-id="30742-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="30742-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30742-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30742-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30742-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30742-113">Remarks</span></span>

<span data-ttu-id="30742-114">Diese Methode wird nur aufgerufen, wenn die Anwendung das Objekt sofort zurück in die Zeitachse einfügt.</span><span class="sxs-lookup"><span data-stu-id="30742-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="30742-115">Es ist ein ungültiger Vorgang, diese Methode aufzurufen, ohne das Objekt dann erneut einzufügen.</span><span class="sxs-lookup"><span data-stu-id="30742-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="30742-116">Um ein Objekt dauerhaft zu entfernen, nennen Sie [**iamtimelineobj:: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="30742-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="30742-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="30742-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30742-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="30742-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30742-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30742-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30742-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30742-120">Requirements</span></span>



| <span data-ttu-id="30742-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30742-121">Requirement</span></span> | <span data-ttu-id="30742-122">Wert</span><span class="sxs-lookup"><span data-stu-id="30742-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30742-123">Header</span><span class="sxs-lookup"><span data-stu-id="30742-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30742-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="30742-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="30742-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30742-125">Library</span></span><br/> | <dl> <span data-ttu-id="30742-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="30742-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30742-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30742-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30742-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30742-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="30742-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="30742-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




