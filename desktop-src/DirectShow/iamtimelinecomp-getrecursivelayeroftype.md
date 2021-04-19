---
description: Die getrecursivelayeroftype-Methode führt eine gründliche Reihenfolge der in dieser Komposition enthaltenen virtuellen Spuren durch und ruft den virtuellen n-ten Titel aus dieser Reihenfolge ab.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Iamtimelinecomp:: getrecursivelayeroftype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362082"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="e52c1-103">Iamtimelinecomp:: getrecursivelayeroftype-Methode</span><span class="sxs-lookup"><span data-stu-id="e52c1-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="e52c1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e52c1-104">\[Deprecated.</span></span> <span data-ttu-id="e52c1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e52c1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e52c1-106">Die `GetRecursiveLayerOfType` -Methode führt eine gründliche Reihenfolge der in dieser Komposition enthaltenen virtuellen Spuren durch und ruft die *n*-te virtuelle Spur aus dieser Reihenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="e52c1-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e52c1-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="e52c1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e52c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e52c1-109">*ppvirtualtrack* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e52c1-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e52c1-110">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des virtuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="e52c1-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e52c1-111">*Whichlayer*</span><span class="sxs-lookup"><span data-stu-id="e52c1-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="e52c1-112">Gibt an, welche virtuelle Spur abgerufen werden soll, indiziert von NULL.</span><span class="sxs-lookup"><span data-stu-id="e52c1-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="e52c1-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="e52c1-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="e52c1-114">Member des Enumerationstyps für den [**\_ \_ Haupttyp der Zeitachse**](timeline-major-type.md) , der angibt, ob die Suche nachverfolgt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e52c1-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e52c1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e52c1-115">Return value</span></span>

<span data-ttu-id="e52c1-116">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="e52c1-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e52c1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e52c1-117">Return code</span></span>                                                                                  | <span data-ttu-id="e52c1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e52c1-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="e52c1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e52c1-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e52c1-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e52c1-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="e52c1-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e52c1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e52c1-122">Kein Objekt vom angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="e52c1-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="e52c1-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e52c1-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e52c1-124">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="e52c1-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="e52c1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e52c1-125">Remarks</span></span>

<span data-ttu-id="e52c1-126">In der Regel ist es nicht erforderlich, dass eine Anwendung diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="e52c1-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="e52c1-127">Wenn es sich bei dem *Typparameter* um einen Zeitachse \_ \_ -Haupttyp \_ Track handelt, umfasst die Tiefe der ersten Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e52c1-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="e52c1-128">Wenn dies nicht der Fall ist, enthält Sie nur die Komposition und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="e52c1-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="e52c1-129">Das Objekt selbst ist in der Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="e52c1-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="e52c1-130">In der folgenden Anordnung, beginnend bei der Komposition A, wäre die Reihenfolge z. B. B, C, F, D, E, a.</span><span class="sxs-lookup"><span data-stu-id="e52c1-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="e52c1-132">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="e52c1-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e52c1-133">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="e52c1-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e52c1-134">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e52c1-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e52c1-135">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e52c1-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e52c1-136">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e52c1-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e52c1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e52c1-137">Requirements</span></span>



| <span data-ttu-id="e52c1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e52c1-138">Requirement</span></span> | <span data-ttu-id="e52c1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e52c1-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e52c1-140">Header</span><span class="sxs-lookup"><span data-stu-id="e52c1-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e52c1-141"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e52c1-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e52c1-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e52c1-142">Library</span></span><br/> | <dl> <span data-ttu-id="e52c1-143"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e52c1-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e52c1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e52c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52c1-145">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e52c1-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="e52c1-146">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e52c1-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




