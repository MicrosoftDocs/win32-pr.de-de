---
title: Iwmpquery beginnextgroup-Methode
description: Die beginnextgroup-Methode beginnt mit einer neuen Bedingungs Gruppe. | Iwmpquery beginnextgroup-Methode
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- beginnextgroup-Methode, Windows-Media Player
- beginnextgroup-Methode, Windows Media Player, iwmpquery-Schnittstelle
- Iwmpquery Interface, Windows Media Player, beginnextgroup-Methode
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352029"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="f3a24-107">Iwmpquery:: beginnextgroup-Methode</span><span class="sxs-lookup"><span data-stu-id="f3a24-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="f3a24-108">Die **beginnextgroup** -Methode beginnt mit einer neuen Bedingungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f3a24-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a24-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a24-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="f3a24-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3a24-110">Parameters</span></span>

<span data-ttu-id="f3a24-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f3a24-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3a24-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3a24-112">Return value</span></span>

<span data-ttu-id="f3a24-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f3a24-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a24-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a24-114">Remarks</span></span>

<span data-ttu-id="f3a24-115">Das Starten einer neuen Bedingungs Gruppe impliziert, dass Sie die aktuelle Bedingungs Gruppe abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="f3a24-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="f3a24-116">Die neue Bedingungs Gruppe wird immer mit der- **oder** -Logik mit der vorherigen Bedingungs Gruppe verkettet.</span><span class="sxs-lookup"><span data-stu-id="f3a24-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="f3a24-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3a24-117">Examples</span></span>

<span data-ttu-id="f3a24-118">Im folgenden Beispiel wird eine komplexe Abfrage erstellt, indem zwei Gruppen durchlaufen werden, die jeweils eine Bedingung enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3a24-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="f3a24-119">Die Ergebnisse der Abfrage werden als Zeichen folgen Sammlung extrahiert und in einem Listenfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3a24-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="f3a24-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f3a24-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="f3a24-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a24-121">Requirements</span></span>



| <span data-ttu-id="f3a24-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a24-122">Requirement</span></span> | <span data-ttu-id="f3a24-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a24-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a24-124">Version</span><span class="sxs-lookup"><span data-stu-id="f3a24-124">Version</span></span><br/>   | <span data-ttu-id="f3a24-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f3a24-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f3a24-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3a24-126">Namespace</span></span><br/> | <span data-ttu-id="f3a24-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f3a24-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f3a24-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="f3a24-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3a24-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3a24-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a24-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a24-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a24-131">**IWMPMediaCollection2. kreatequery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f3a24-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3a24-132">**IWMPMediaCollection2. getplaylistbyquery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f3a24-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3a24-133">**IWMPMediaCollection2. getstringcollectionbyquery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f3a24-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3a24-134">**Iwmpquery-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f3a24-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





