---
title: Iwmpmedia ismembership of-Methode
description: Die ismembership of-Methode gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- ismembership of-Methode, Windows-Media Player
- ismembership of-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, ismembership of-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358745"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="394e7-106">Iwmpmedia:: ismembership of-Methode</span><span class="sxs-lookup"><span data-stu-id="394e7-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="394e7-107">Die **ismembership of** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="394e7-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="394e7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="394e7-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="394e7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="394e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="394e7-110">*pwiedergabe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="394e7-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394e7-111">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="394e7-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="394e7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="394e7-112">Return value</span></span>

<span data-ttu-id="394e7-113">Ein **System. Boolean** -Wert, der angibt, ob das Medien Element ein Member der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="394e7-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="394e7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="394e7-114">Remarks</span></span>

<span data-ttu-id="394e7-115">Diese Methode kann die von der **iwmpmediacollection** -Schnittstelle abgerufenen Wiedergabelisten nicht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="394e7-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="394e7-116">Um zu testen, ob ein Medien Element ein Member einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabelisten Auflistung mit der Eigenschaft **AxWindowsMediaPlayer. playlistcollection** ab.</span><span class="sxs-lookup"><span data-stu-id="394e7-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="394e7-117">Nachdem Sie die Auflistung abgerufen haben, rufen Sie die einzelne Wiedergabeliste durch Aufrufen der **iwmpplaylistcollection. getByName** -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="394e7-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="394e7-118">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="394e7-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="394e7-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="394e7-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="394e7-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="394e7-120">Examples</span></span>

<span data-ttu-id="394e7-121">Im folgenden Beispiel wird **ismembership of** verwendet, um zu testen, ob das aktuelle Medien Element ein Member der Wiedergabeliste mit dem Namen alle Musik ist.</span><span class="sxs-lookup"><span data-stu-id="394e7-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="394e7-122">Wenn dies nicht der Fall ist, wird das aktuelle Medien Element an die Wiedergabeliste angehängt.</span><span class="sxs-lookup"><span data-stu-id="394e7-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="394e7-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="394e7-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="394e7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="394e7-124">Requirements</span></span>



| <span data-ttu-id="394e7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="394e7-125">Requirement</span></span> | <span data-ttu-id="394e7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="394e7-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394e7-127">Version</span><span class="sxs-lookup"><span data-stu-id="394e7-127">Version</span></span><br/>   | <span data-ttu-id="394e7-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="394e7-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="394e7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="394e7-129">Namespace</span></span><br/> | <span data-ttu-id="394e7-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="394e7-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="394e7-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="394e7-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="394e7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="394e7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394e7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="394e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394e7-134">**AxWindowsMediaPlayer. playlistcollection (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="394e7-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="394e7-135">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="394e7-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="394e7-136">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="394e7-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="394e7-137">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="394e7-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





