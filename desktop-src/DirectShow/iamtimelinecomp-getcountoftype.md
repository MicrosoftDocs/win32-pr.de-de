---
description: Die getzählto ftype-Methode ruft die Anzahl der Objekte eines angegebenen Typs, die in dieser Komposition enthalten ist, und alle zugehörigen virtuellen Spuren rekursiv ab.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Iamtimelinecomp:: getzählype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356049"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="5ac20-103">Iamtimelinecomp:: getzählype-Methode</span><span class="sxs-lookup"><span data-stu-id="5ac20-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="5ac20-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5ac20-104">\[Deprecated.</span></span> <span data-ttu-id="5ac20-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5ac20-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ac20-106">Die `GetCountOfType` -Methode ruft die Anzahl der Objekte eines angegebenen Typs, die in dieser Komposition enthalten ist, und alle zugehörigen virtuellen Spuren rekursiv ab.</span><span class="sxs-lookup"><span data-stu-id="5ac20-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac20-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ac20-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="5ac20-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ac20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac20-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="5ac20-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac20-110">Empfängt rekursiv die Anzahl der Objekte des angegebenen Typs, die in dieser Komposition und allen virtuellen Spuren enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5ac20-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="5ac20-111">*pvalwithcomps*</span><span class="sxs-lookup"><span data-stu-id="5ac20-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac20-112">Empfängt die Anzahl, die in *PVal* zurückgegeben wurde, sowie die Anzahl der durchsuchten Kompositionen, einschließlich dieses.</span><span class="sxs-lookup"><span data-stu-id="5ac20-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="5ac20-113">*Majortype*</span><span class="sxs-lookup"><span data-stu-id="5ac20-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac20-114">Member des enumerierten Typs der [**Zeitachse \_ \_**](timeline-major-type.md) , der den Typ des zu zählenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="5ac20-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac20-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ac20-115">Return value</span></span>

<span data-ttu-id="5ac20-116">Gibt " \_ OK" zurück, wenn erfolgreich, andernfalls einen E- \_ Zeiger.</span><span class="sxs-lookup"><span data-stu-id="5ac20-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac20-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ac20-117">Remarks</span></span>

<span data-ttu-id="5ac20-118">In der Regel Ruft eine Anwendung diese Methode nicht auf.</span><span class="sxs-lookup"><span data-stu-id="5ac20-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="5ac20-119">Sie wird von der Rendering-Engine aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ac20-119">It is called by the render engine.</span></span>

<span data-ttu-id="5ac20-120">Wenn Sie die Komposition zählen, ist der in *PVal* zurückgegebene Wert 0 (null), und der in *pvalwithcomps* zurückgegebene Wert ist die Anzahl der Kompositionen.</span><span class="sxs-lookup"><span data-stu-id="5ac20-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="5ac20-121">Der Wert von *\* pvalwithcomps* enthält die Komposition, auf der Sie die Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ac20-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="5ac20-122">Wenn Sie diese Methode z. b. für eine leere Komposition aufzurufen, ist *\* pvalwithcomps* gleich 1.</span><span class="sxs-lookup"><span data-stu-id="5ac20-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="5ac20-123">Gruppen dürfen sich nicht innerhalb von Kompositionen befinden, daher können Sie diese Methode nicht zum zählen von Gruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ac20-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="5ac20-124">(Die zurückgegebene Anzahl ist immer 0 (null).) Um Gruppen zu zählen, können Sie die [**iamtimeline:: getgroupcount**](iamtimeline-getgroupcount.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5ac20-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="5ac20-125">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5ac20-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ac20-126">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5ac20-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ac20-127">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5ac20-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ac20-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ac20-128">Requirements</span></span>



| <span data-ttu-id="5ac20-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ac20-129">Requirement</span></span> | <span data-ttu-id="5ac20-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5ac20-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac20-131">Header</span><span class="sxs-lookup"><span data-stu-id="5ac20-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5ac20-132"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5ac20-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ac20-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ac20-133">Library</span></span><br/> | <dl> <span data-ttu-id="5ac20-134"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5ac20-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac20-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ac20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac20-136">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ac20-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="5ac20-137">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5ac20-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




