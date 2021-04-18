---
title: Iwmpplaylistcollection getByName-Methode
description: Die getByName-Methode gibt eine iwmpplaylistarray-Schnittstelle zurück, die Zugriff auf Wiedergabelisten mit dem angegebenen Namen bietet, sofern vorhanden.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, getByName-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352064"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="966f0-106">Iwmpplaylistcollection:: getByName-Methode</span><span class="sxs-lookup"><span data-stu-id="966f0-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="966f0-107">Die **getByName** -Methode gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf Wiedergabelisten mit dem angegebenen Namen bietet, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="966f0-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="966f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="966f0-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="966f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="966f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="966f0-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="966f0-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="966f0-111">Ein **System. String** -Wert, der der Name der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="966f0-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="966f0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="966f0-112">Return value</span></span>

<span data-ttu-id="966f0-113">Eine **WMPLib. iwmpplaylistarray** -Schnittstelle für das abgerufene Array von Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="966f0-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="966f0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="966f0-114">Remarks</span></span>

<span data-ttu-id="966f0-115">Verwenden Sie **iwmpplaylistarray. count** , um zu bestimmen, ob eine Wiedergabeliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="966f0-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="966f0-116">Wenn **count** 0 (null) ist, ist das Array leer.</span><span class="sxs-lookup"><span data-stu-id="966f0-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="966f0-117">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="966f0-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="966f0-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="966f0-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="966f0-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="966f0-119">Examples</span></span>

<span data-ttu-id="966f0-120">Im folgenden Beispiel wird **getByName** verwendet, um die Wiedergabelisten Auflistung auf eine Wiedergabeliste mit dem Namen "Favoriten--4 und 5 Sterne bewertet" zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="966f0-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="966f0-121">Wenn eine Wiedergabeliste mit diesem Namen vorhanden ist, wird Sie von **getByName** als aktuelle Wiedergabeliste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="966f0-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="966f0-122">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="966f0-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="966f0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="966f0-123">Requirements</span></span>



| <span data-ttu-id="966f0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="966f0-124">Requirement</span></span> | <span data-ttu-id="966f0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="966f0-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="966f0-126">Version</span><span class="sxs-lookup"><span data-stu-id="966f0-126">Version</span></span><br/>   | <span data-ttu-id="966f0-127">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="966f0-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="966f0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="966f0-128">Namespace</span></span><br/> | <span data-ttu-id="966f0-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="966f0-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="966f0-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="966f0-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="966f0-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="966f0-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="966f0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="966f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="966f0-133">**Iwmpplaylistarray-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="966f0-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="966f0-134">**Iwmpplaylistarray. Count (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="966f0-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="966f0-135">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="966f0-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





