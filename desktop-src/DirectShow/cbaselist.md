---
description: Die cbaselist-Methode implementiert eine abtraktions Liste. Die cgenericlist-Klassen Vorlage, die von cbaselist abgeleitet wird, bietet eine Typüberprüfung und eine einfachere Schnittstelle als die cbaselist-Klasse.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Cbaselist-Klasse (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372266"
---
# <a name="cbaselist-class"></a><span data-ttu-id="eded9-104">Cbaselist-Klasse</span><span class="sxs-lookup"><span data-stu-id="eded9-104">CBaseList class</span></span>

![cbaselist-Klassenhierarchie](images/list01.png)

<span data-ttu-id="eded9-106">Die **cbaselist** -Methode implementiert eine abtraktions Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="eded9-107">Die [**cgenericlist**](cgenericlist.md) -Klassen Vorlage, die von **cbaselist** abgeleitet wird, bietet eine Typüberprüfung und eine einfachere Schnittstelle als die **cbaselist** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="eded9-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="eded9-108">Die **cbaselist** -Klasse wird nach der **CObList** -Klasse in der MFC-Bibliothek (Microsoft Foundation Classes) modelliert.</span><span class="sxs-lookup"><span data-stu-id="eded9-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="eded9-109">Positionen in der Liste werden durch eine Positions Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eded9-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="eded9-110">Der Aufrufer sollte nicht auf die internen Member der Positions Struktur zugreifen. behandeln Sie ihn als Zeiger auf einen Listen Knoten.</span><span class="sxs-lookup"><span data-stu-id="eded9-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="eded9-111">Die Position eines Objekts in der Liste bleibt gültig, bis das Objekt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="eded9-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="eded9-112">Die Liste erfordert keine Unterstützung durch die darin enthaltenen Objekte.</span><span class="sxs-lookup"><span data-stu-id="eded9-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="eded9-113">Es führt keine Speicherverwaltung oder das Kopieren der Objekte durch.</span><span class="sxs-lookup"><span data-stu-id="eded9-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="eded9-114">Objekte können mehrere Listen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eded9-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="eded9-115">Ungefähr die Hälfte der Methoden in dieser Klasse agieren auf einzelne Objekte.</span><span class="sxs-lookup"><span data-stu-id="eded9-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="eded9-116">Diese Methoden haben das Suffix-I im Methodennamen.</span><span class="sxs-lookup"><span data-stu-id="eded9-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="eded9-117">Die anderen Methoden wirken sich auf ganze Listen aus.</span><span class="sxs-lookup"><span data-stu-id="eded9-117">The other methods act on entire lists.</span></span> <span data-ttu-id="eded9-118">Beispielsweise fügt die [**cbaselist:: AddAfter**](cbaselist-addafter.md) -Methode eine Liste an eine andere Liste an.</span><span class="sxs-lookup"><span data-stu-id="eded9-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="eded9-119">Einzelobjekt Vorgänge geben Positionswerte oder **null** bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="eded9-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="eded9-120">Listen Vorgänge geben **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="eded9-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="eded9-121">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="eded9-121">Protected Member Variables</span></span>                             | <span data-ttu-id="eded9-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eded9-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="eded9-123">**m- \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="eded9-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="eded9-124">Anzahl der Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="eded9-125">**m \_ pfirst**</span><span class="sxs-lookup"><span data-stu-id="eded9-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="eded9-126">Zeiger auf den ersten Knoten in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="eded9-127">**m- \_ pLast**</span><span class="sxs-lookup"><span data-stu-id="eded9-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="eded9-128">Zeiger auf den letzten Knoten in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="eded9-129">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="eded9-129">Protected Methods</span></span>                                      | <span data-ttu-id="eded9-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eded9-130">Description</span></span>                                                               |
| [<span data-ttu-id="eded9-131">**Getnexti**</span><span class="sxs-lookup"><span data-stu-id="eded9-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="eded9-132">Ruft das Element an der angegebenen Position ab und erhöht die Position.</span><span class="sxs-lookup"><span data-stu-id="eded9-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="eded9-133">**TIS**</span><span class="sxs-lookup"><span data-stu-id="eded9-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="eded9-134">Ruft das Element an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="eded9-135">**Findi**</span><span class="sxs-lookup"><span data-stu-id="eded9-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="eded9-136">Ruft die erste Position ab, die das angegebene Element enthält.</span><span class="sxs-lookup"><span data-stu-id="eded9-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="eded9-137">**Removeheadi**</span><span class="sxs-lookup"><span data-stu-id="eded9-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="eded9-138">Entfernt das erste Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="eded9-139">**Removetaili**</span><span class="sxs-lookup"><span data-stu-id="eded9-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="eded9-140">Entfernt das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="eded9-141">**Removei**</span><span class="sxs-lookup"><span data-stu-id="eded9-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="eded9-142">Entfernt das Element an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="eded9-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="eded9-143">**Addtaili**</span><span class="sxs-lookup"><span data-stu-id="eded9-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="eded9-144">Fügt ein Element am Ende der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="eded9-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="eded9-145">**Addheadi**</span><span class="sxs-lookup"><span data-stu-id="eded9-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="eded9-146">Fügt ein Element am Anfang der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="eded9-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="eded9-147">**Addaf-i**</span><span class="sxs-lookup"><span data-stu-id="eded9-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="eded9-148">Fügt ein Element nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="eded9-149">**Addbeforei**</span><span class="sxs-lookup"><span data-stu-id="eded9-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="eded9-150">Fügt ein Element vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="eded9-151">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="eded9-151">Public Methods</span></span>                                         | <span data-ttu-id="eded9-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eded9-152">Description</span></span>                                                               |
| [<span data-ttu-id="eded9-153">**Cbaselist**</span><span class="sxs-lookup"><span data-stu-id="eded9-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="eded9-154">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eded9-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="eded9-155">**~ Cbaselist**</span><span class="sxs-lookup"><span data-stu-id="eded9-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="eded9-156">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eded9-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="eded9-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="eded9-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="eded9-158">Entfernt alle Knoten aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="eded9-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="eded9-159">**Gezeige adpositioni**</span><span class="sxs-lookup"><span data-stu-id="eded9-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="eded9-160">Ruft die Position des ersten Elements in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="eded9-161">**Gettailpositioni**</span><span class="sxs-lookup"><span data-stu-id="eded9-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="eded9-162">Ruft die Position des letzten Elements der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="eded9-163">**Getgräfin**</span><span class="sxs-lookup"><span data-stu-id="eded9-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="eded9-164">Ruft die Anzahl der Elemente in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="eded9-165">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="eded9-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="eded9-166">Ruft die nächste Position in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="eded9-167">**Prev**</span><span class="sxs-lookup"><span data-stu-id="eded9-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="eded9-168">Ruft die vorherige Position in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="eded9-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="eded9-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="eded9-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="eded9-170">Fügt eine weitere Liste am Anfang der Liste ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="eded9-171">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="eded9-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="eded9-172">Fügt am Ende dieser Liste eine andere Liste an.</span><span class="sxs-lookup"><span data-stu-id="eded9-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="eded9-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="eded9-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="eded9-174">Fügt eine Liste nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="eded9-175">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="eded9-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="eded9-176">Fügt eine Liste vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="eded9-177">**"Muveum"**</span><span class="sxs-lookup"><span data-stu-id="eded9-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="eded9-178">Teilt die Liste und fügt den Head-Teil an das Ende einer anderen Liste an.</span><span class="sxs-lookup"><span data-stu-id="eded9-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="eded9-179">**In den Kopf**</span><span class="sxs-lookup"><span data-stu-id="eded9-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="eded9-180">Teilt die Liste auf und fügt den Teil Fragment an der Spitze einer anderen Liste ein.</span><span class="sxs-lookup"><span data-stu-id="eded9-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="eded9-181">**Umgekehr**</span><span class="sxs-lookup"><span data-stu-id="eded9-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="eded9-182">Kehrt die Reihenfolge der Liste um.</span><span class="sxs-lookup"><span data-stu-id="eded9-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="eded9-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eded9-183">Requirements</span></span>



| <span data-ttu-id="eded9-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eded9-184">Requirement</span></span> | <span data-ttu-id="eded9-185">Wert</span><span class="sxs-lookup"><span data-stu-id="eded9-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eded9-186">Header</span><span class="sxs-lookup"><span data-stu-id="eded9-186">Header</span></span><br/>  | <dl> <span data-ttu-id="eded9-187"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eded9-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eded9-188">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eded9-188">Library</span></span><br/> | <dl> <span data-ttu-id="eded9-189">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eded9-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eded9-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eded9-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eded9-191">DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="eded9-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




