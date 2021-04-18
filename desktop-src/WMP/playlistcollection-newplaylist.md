---
title: Playlistcollection. newwiedergabe-Methode
description: Die newwiedergabe-Methode erstellt eine neue Wiedergabeliste in der Bibliothek.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371690"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="ab275-106">Playlistcollection. newwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="ab275-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="ab275-107">Die **newwiedergabe** -Methode erstellt eine neue Wiedergabeliste in der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="ab275-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab275-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab275-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="ab275-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab275-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab275-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab275-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab275-111">**Zeichenfolge** , die den Namen der zu erstellenden Wiedergabeliste enthält.</span><span class="sxs-lookup"><span data-stu-id="ab275-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab275-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab275-112">Return value</span></span>

<span data-ttu-id="ab275-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ab275-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab275-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab275-114">Remarks</span></span>

<span data-ttu-id="ab275-115">Diese Methode erstellt eine leere Wiedergabeliste in der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="ab275-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="ab275-116">Verwenden Sie die *Wiedergabeliste*, um die Wiedergabeliste mit Medien Elementen auszufüllen. **appendItem** oder *Wiedergabeliste*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="ab275-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="ab275-117">In der Bibliothek sind mehrere Wiedergabelisten mit dem gleichen Namen zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab275-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="ab275-118">Verwenden Sie **getByName** und *playlistarray*, um zu vermeiden, dass ein doppelter Wiedergabelisten Name mit dieser Methode erstellt wird. **count** , um zu bestimmen, ob eine Wiedergabeliste mit einem bestimmten Namen bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ab275-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="ab275-119">Führende und nachfolgende Leerzeichen sind in Wiedergabelisten Namen nicht zulässig und werden automatisch aus dem für den *Name* -Parameter angegebenen Wert entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab275-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="ab275-120">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ab275-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="ab275-121">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ab275-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ab275-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab275-122">Examples</span></span>

<span data-ttu-id="ab275-123">Im folgenden JScript-Beispiel wird eine neue leere Wiedergabeliste mit dem Namen "threelist" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab275-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="ab275-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab275-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="ab275-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab275-125">Requirements</span></span>



| <span data-ttu-id="ab275-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab275-126">Requirement</span></span> | <span data-ttu-id="ab275-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ab275-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab275-128">Version</span><span class="sxs-lookup"><span data-stu-id="ab275-128">Version</span></span><br/> | <span data-ttu-id="ab275-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ab275-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ab275-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ab275-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab275-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab275-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab275-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab275-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab275-133">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="ab275-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="ab275-134">**Wiedergabeliste. appendItem**</span><span class="sxs-lookup"><span data-stu-id="ab275-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="ab275-135">**Wiedergabeliste. InsertItem**</span><span class="sxs-lookup"><span data-stu-id="ab275-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="ab275-136">**Playlistarray. Count**</span><span class="sxs-lookup"><span data-stu-id="ab275-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="ab275-137">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ab275-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ab275-138">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="ab275-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="ab275-139">**Playlistcollection. importwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="ab275-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="ab275-140">**Playlistcollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="ab275-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="ab275-141">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="ab275-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ab275-142">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="ab275-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





