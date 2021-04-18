---
description: Die cgenericlist-Klassen Vorlage, die eine typspezifische Liste implementiert. Weitere Informationen finden Sie unter cbaselist.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Cgenericlist-Klasse (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371626"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="6d267-104">Cgenericlist-Klasse</span><span class="sxs-lookup"><span data-stu-id="6d267-104">CGenericList class</span></span>

![cgenericlist-Klassenhierarchie](images/list01.png)

<span data-ttu-id="6d267-106">Die `CGenericList` Klassen Vorlage, die eine typspezifische Liste implementiert.</span><span class="sxs-lookup"><span data-stu-id="6d267-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="6d267-107">Weitere Informationen finden Sie unter [**cbaselist**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="6d267-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="6d267-108">Um diese Vorlage zu verwenden, deklarieren Sie eine Variable vom Typ `CGenericList` mit einem Vorlagen Argument, das den Objekttyp in der Liste definiert.</span><span class="sxs-lookup"><span data-stu-id="6d267-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="6d267-109">Die folgende Anweisung deklariert beispielsweise eine Liste von [**cbasefilter**](cbasefilter.md) -Objekten:</span><span class="sxs-lookup"><span data-stu-id="6d267-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="6d267-110">Aus praktischer Gründen definiert wxlist. h die folgenden Listen Typen:</span><span class="sxs-lookup"><span data-stu-id="6d267-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="6d267-111">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="6d267-111">Public Methods</span></span>                                          | <span data-ttu-id="6d267-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d267-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="6d267-113">**Cgenericlist**</span><span class="sxs-lookup"><span data-stu-id="6d267-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="6d267-114">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6d267-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="6d267-115">**~ Cgenericlist**</span><span class="sxs-lookup"><span data-stu-id="6d267-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="6d267-116">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6d267-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="6d267-117">**Gezeige-Position**</span><span class="sxs-lookup"><span data-stu-id="6d267-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="6d267-118">Ruft die Position des ersten Elements in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="6d267-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="6d267-119">**Gettailposition**</span><span class="sxs-lookup"><span data-stu-id="6d267-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="6d267-120">Ruft die Position des letzten Elements der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="6d267-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="6d267-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="6d267-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="6d267-122">Ruft die Anzahl der Elemente in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="6d267-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="6d267-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="6d267-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="6d267-124">Ruft das Element an der angegebenen Position ab und erhöht die Position.</span><span class="sxs-lookup"><span data-stu-id="6d267-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="6d267-125">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="6d267-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="6d267-126">Ruft das Element an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="6d267-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="6d267-127">**Gezeige AD**</span><span class="sxs-lookup"><span data-stu-id="6d267-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="6d267-128">Ruft das Element am Anfang der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="6d267-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="6d267-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="6d267-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="6d267-130">Entfernt das erste Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6d267-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="6d267-131">**Removetail**</span><span class="sxs-lookup"><span data-stu-id="6d267-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="6d267-132">Entfernt das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6d267-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="6d267-133">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="6d267-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="6d267-134">Entfernt das Element an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="6d267-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="6d267-135">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="6d267-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="6d267-136">Fügt ein Element oder eine Liste vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="6d267-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="6d267-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="6d267-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="6d267-138">Fügt ein Element oder eine Liste nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="6d267-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="6d267-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="6d267-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="6d267-140">Fügt ein Element oder eine Liste am Anfang der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d267-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="6d267-141">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="6d267-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="6d267-142">Fügt ein Element oder eine Liste an das Ende der Liste an.</span><span class="sxs-lookup"><span data-stu-id="6d267-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="6d267-143">**Sich**</span><span class="sxs-lookup"><span data-stu-id="6d267-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="6d267-144">Ruft die erste Position ab, die das angegebene Element enthält.</span><span class="sxs-lookup"><span data-stu-id="6d267-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="6d267-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d267-145">Requirements</span></span>



| <span data-ttu-id="6d267-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d267-146">Requirement</span></span> | <span data-ttu-id="6d267-147">Wert</span><span class="sxs-lookup"><span data-stu-id="6d267-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d267-148">Header</span><span class="sxs-lookup"><span data-stu-id="6d267-148">Header</span></span><br/>  | <dl> <span data-ttu-id="6d267-149"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d267-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6d267-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d267-150">Library</span></span><br/> | <dl> <span data-ttu-id="6d267-151">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6d267-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




