---
description: Die getzählto ftype-Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Iamtimeline:: getzählto ftype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370638"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="63f35-103">Iamtimeline:: getzählto ftype-Methode</span><span class="sxs-lookup"><span data-stu-id="63f35-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="63f35-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="63f35-104">\[Deprecated.</span></span> <span data-ttu-id="63f35-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="63f35-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="63f35-106">Die `GetCountOfType` -Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="63f35-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f35-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63f35-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="63f35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63f35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f35-109">*Gruppieren*</span><span class="sxs-lookup"><span data-stu-id="63f35-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="63f35-110">Index Nummer der Gruppe, für die die Anzahl abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="63f35-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="63f35-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="63f35-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="63f35-112">Empfängt rekursiv die Anzahl von Objekten des angegebenen Typs, die in der Gruppe enthalten sind, und alle zugehörigen virtuellen Spuren.</span><span class="sxs-lookup"><span data-stu-id="63f35-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="63f35-113">*pvalwithcomps*</span><span class="sxs-lookup"><span data-stu-id="63f35-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="63f35-114">Empfängt die Anzahl, die in *PVal* zurückgegeben wurde, sowie die Anzahl der durchsuchten Kompositionen, einschließlich dieses.</span><span class="sxs-lookup"><span data-stu-id="63f35-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="63f35-115">*Majortype*</span><span class="sxs-lookup"><span data-stu-id="63f35-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="63f35-116">Member des enumerierten Typs der [**Zeitachse \_ \_**](timeline-major-type.md) , der den Typ des zu zählenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="63f35-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f35-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63f35-117">Return value</span></span>

<span data-ttu-id="63f35-118">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="63f35-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="63f35-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="63f35-119">Return code</span></span>                                                                                  | <span data-ttu-id="63f35-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63f35-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="63f35-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63f35-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="63f35-122">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="63f35-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="63f35-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="63f35-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="63f35-124">Ungültige Gruppennummer.</span><span class="sxs-lookup"><span data-stu-id="63f35-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="63f35-125"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="63f35-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="63f35-126">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="63f35-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63f35-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63f35-127">Remarks</span></span>

<span data-ttu-id="63f35-128">Das Aufrufen dieser Methode entspricht dem Aufrufen von [**iamtimelinecomp:: getzählype**](iamtimelinecomp-getcountoftype.md) für die angegebene Gruppe.</span><span class="sxs-lookup"><span data-stu-id="63f35-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="63f35-129">Weitere Informationen finden Sie im Abschnitt "Hinweise" dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="63f35-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="63f35-130">In der Regel Ruft eine Anwendung diese Methode nicht auf.</span><span class="sxs-lookup"><span data-stu-id="63f35-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="63f35-131">Sie wird intern von der Rendering-Engine aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="63f35-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="63f35-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="63f35-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="63f35-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="63f35-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="63f35-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63f35-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63f35-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63f35-135">Requirements</span></span>



| <span data-ttu-id="63f35-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63f35-136">Requirement</span></span> | <span data-ttu-id="63f35-137">Wert</span><span class="sxs-lookup"><span data-stu-id="63f35-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63f35-138">Header</span><span class="sxs-lookup"><span data-stu-id="63f35-138">Header</span></span><br/>  | <dl> <span data-ttu-id="63f35-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="63f35-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="63f35-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63f35-140">Library</span></span><br/> | <dl> <span data-ttu-id="63f35-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="63f35-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f35-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63f35-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f35-143">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="63f35-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="63f35-144">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="63f35-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




