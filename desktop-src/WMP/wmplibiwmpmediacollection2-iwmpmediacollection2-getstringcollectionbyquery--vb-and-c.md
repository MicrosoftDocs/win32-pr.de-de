---
title: IWMPMediaCollection2 getstringcollectionbyquery-Methode
description: Die getstringcollectionbyquery-Methode gibt eine iwmpstringcollection-Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- getstringcollectionbyquery-Methode, Windows-Media Player
- getstringcollectionbyquery-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getstringcollectionbyquery-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366729"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="95bfd-106">IWMPMediaCollection2:: getstringcollectionbyquery-Methode</span><span class="sxs-lookup"><span data-stu-id="95bfd-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="95bfd-107">Die- `getStringCollectionByQuery` Methode gibt eine **iwmpstringcollection** -Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="95bfd-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bfd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bfd-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="95bfd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bfd-110">*bstrattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95bfd-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bfd-111">Der **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="95bfd-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="95bfd-112">*pquery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95bfd-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bfd-113">Die **WMPLib. iwmpquery** -Schnittstelle, bei der es sich um die Abfrage handelt, die die zum Abrufen der Zeichen folgen Auflistung verwendeten Bedingungen definiert.</span><span class="sxs-lookup"><span data-stu-id="95bfd-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="95bfd-114">*bstraumediatype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95bfd-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bfd-115">Die **System. String** , die den Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="95bfd-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="95bfd-116">Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="95bfd-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="95bfd-117">*bstrausortattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95bfd-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bfd-118">Die **System. String** , die der für die Sortierung verwendete Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="95bfd-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="95bfd-119">Eine Zeichenfolge der Länge 0 (null) bedeutet, dass keine Sortierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="95bfd-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="95bfd-120">*fsortascending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95bfd-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bfd-121">Der **System. Boolean** -Wert, der angibt, ob der Satz von Zeichen folgen Werten in aufsteigender Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="95bfd-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bfd-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95bfd-122">Return value</span></span>

<span data-ttu-id="95bfd-123">Eine **WMPLib. iwmpstringcollection** -Schnittstelle für den abgerufenen Satz von Zeichen folgen Werten.</span><span class="sxs-lookup"><span data-stu-id="95bfd-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bfd-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95bfd-124">Remarks</span></span>

<span data-ttu-id="95bfd-125">Bei Verbund Abfragen mit **iwmpquery** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="95bfd-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="95bfd-126">Wenn die durch den *pquery* -Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="95bfd-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="95bfd-127">Der Wert für den *bstraumediatype* -Parameter wird immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="95bfd-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="95bfd-128">Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *botmediatype* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="95bfd-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bfd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95bfd-129">Requirements</span></span>



| <span data-ttu-id="95bfd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95bfd-130">Requirement</span></span> | <span data-ttu-id="95bfd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="95bfd-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95bfd-132">Version</span><span class="sxs-lookup"><span data-stu-id="95bfd-132">Version</span></span><br/>   | <span data-ttu-id="95bfd-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="95bfd-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="95bfd-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="95bfd-134">Namespace</span></span><br/> | <span data-ttu-id="95bfd-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="95bfd-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="95bfd-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="95bfd-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95bfd-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="95bfd-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bfd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95bfd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bfd-139">**IWMPMediaCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95bfd-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95bfd-140">**Iwmpquery-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95bfd-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95bfd-141">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="95bfd-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95bfd-142">**MediaType-Attribut**</span><span class="sxs-lookup"><span data-stu-id="95bfd-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





