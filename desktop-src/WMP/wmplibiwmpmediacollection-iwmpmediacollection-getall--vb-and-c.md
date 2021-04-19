---
title: Iwmpmediacollection GetAll-Methode
description: Die GetAll-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die der Wiedergabeliste entspricht, die alle Medienelemente in der Bibliothek enthält.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- GetAll-Methoden Fenster Media Player
- GetAll-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, GetAll-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365390"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="ae654-106">Iwmpmediacollection:: GetAll-Methode</span><span class="sxs-lookup"><span data-stu-id="ae654-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="ae654-107">Die **GetAll** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die der Wiedergabeliste entspricht, die alle Medienelemente in der Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="ae654-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae654-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae654-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="ae654-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae654-109">Parameters</span></span>

<span data-ttu-id="ae654-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae654-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae654-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae654-111">Return value</span></span>

<span data-ttu-id="ae654-112">Die **WMPLib. iwmpwiedergabe** -Schnittstelle für die Wiedergabeliste, die alle angeforderten Medienelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="ae654-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae654-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae654-113">Remarks</span></span>

<span data-ttu-id="ae654-114">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="ae654-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ae654-115">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ae654-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ae654-116">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der **GetAll** -Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae654-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="ae654-117">Wenn Sie die Schnittstelle durch Aufrufen von [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abrufen, gibt die **GetAll** -Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="ae654-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="ae654-118">Wenn Sie jedoch die Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, gibt die **GetAll** -Methode nur die Audioelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="ae654-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="ae654-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae654-119">Examples</span></span>

<span data-ttu-id="ae654-120">Im folgenden Beispiel wird **GetAll** verwendet, um Medienelemente nach dem Zufallsprinzip aus der Medien Auflistung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="ae654-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="ae654-121">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ae654-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="ae654-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae654-122">Requirements</span></span>



| <span data-ttu-id="ae654-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae654-123">Requirement</span></span> | <span data-ttu-id="ae654-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ae654-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae654-125">Version</span><span class="sxs-lookup"><span data-stu-id="ae654-125">Version</span></span><br/>   | <span data-ttu-id="ae654-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ae654-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ae654-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae654-127">Namespace</span></span><br/> | <span data-ttu-id="ae654-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ae654-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ae654-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="ae654-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ae654-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ae654-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae654-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae654-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae654-132">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ae654-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae654-133">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ae654-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





