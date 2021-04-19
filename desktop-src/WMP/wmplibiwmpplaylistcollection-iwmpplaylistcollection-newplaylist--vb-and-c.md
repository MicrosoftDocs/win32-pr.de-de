---
title: Iwmpplaylistcollection newwiedergabe-Methode
description: Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue, leere Wiedergabeliste in der Bibliothek zurück.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367543"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="e76eb-106">Iwmpplaylistcollection:: newwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="e76eb-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="e76eb-107">Die **newwiedergabe** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle für eine neue, leere Wiedergabeliste in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="e76eb-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e76eb-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="e76eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e76eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76eb-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e76eb-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76eb-111">Ein **System. String** -Wert, der der Name der neuen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="e76eb-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e76eb-112">Return value</span></span>

<span data-ttu-id="e76eb-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die neue Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="e76eb-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e76eb-114">Remarks</span></span>

<span data-ttu-id="e76eb-115">Diese Methode erstellt eine leere Wiedergabeliste in der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e76eb-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="e76eb-116">Um die Wiedergabeliste mit Medien Elementen zu füllen, verwenden Sie **iwmpwiedergabe. appendItem** oder **iwmpwiedergabe. InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="e76eb-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="e76eb-117">In der Bibliothek sind mehrere Wiedergabelisten mit dem gleichen Namen zulässig.</span><span class="sxs-lookup"><span data-stu-id="e76eb-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="e76eb-118">Um zu vermeiden, dass mit dieser Methode ein doppelter Wiedergabelisten Name erstellt wird, verwenden Sie die **getByName** -Methode und **iwmpplaylistarray. count** , um zu ermitteln, ob bereits eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e76eb-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="e76eb-119">Führende und nachfolgende Leerzeichen sind in Wiedergabelisten Namen nicht zulässig und werden automatisch aus dem für den *bstrinname* -Parameter angegebenen Wert entfernt.</span><span class="sxs-lookup"><span data-stu-id="e76eb-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="e76eb-120">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="e76eb-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="e76eb-121">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e76eb-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e76eb-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e76eb-122">Examples</span></span>

<span data-ttu-id="e76eb-123">Im folgenden Beispiel wird eine neue leere Wiedergabeliste mit dem Namen "threelist" erstellt, der Wiedergabeliste hinzugefügt und eine Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e76eb-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="e76eb-124">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e76eb-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="e76eb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e76eb-125">Requirements</span></span>



| <span data-ttu-id="e76eb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e76eb-126">Requirement</span></span> | <span data-ttu-id="e76eb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e76eb-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76eb-128">Version</span><span class="sxs-lookup"><span data-stu-id="e76eb-128">Version</span></span><br/>   | <span data-ttu-id="e76eb-129">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e76eb-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e76eb-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e76eb-130">Namespace</span></span><br/> | <span data-ttu-id="e76eb-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e76eb-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e76eb-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="e76eb-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e76eb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e76eb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76eb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e76eb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76eb-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e76eb-136">**Iwmpwiedergabe. appendItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e76eb-137">**Iwmpwiedergabe. InsertItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e76eb-138">**Iwmpplaylistarray. Count (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e76eb-139">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e76eb-140">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e76eb-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





