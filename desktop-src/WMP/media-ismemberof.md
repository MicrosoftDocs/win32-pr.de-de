---
title: Media. ismembership of-Methode
description: Die ismembership of-Methode gibt einen Wert zurück, der angibt, ob das Medien Element ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- ismembership of-Methode, Windows-Media Player
- ismembership of-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, ismembership of-Methode
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369594"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="7a3c4-106">Media. ismembership of-Methode</span><span class="sxs-lookup"><span data-stu-id="7a3c4-106">Media.isMemberOf method</span></span>

<span data-ttu-id="7a3c4-107">Die **ismembership of** -Methode gibt einen Wert zurück, der angibt, ob das Medien Element ein Member der angegebenen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a3c4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a3c4-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="7a3c4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a3c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a3c4-110">*Wiedergabeliste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a3c4-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a3c4-111">**Wiedergabe** Listen Objekt, das das Medien Element enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a3c4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a3c4-112">Return value</span></span>

<span data-ttu-id="7a3c4-113">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a3c4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a3c4-114">Remarks</span></span>

<span data-ttu-id="7a3c4-115">Diese Methode kann keine Wiedergabelisten überprüfen, die über das **mediacollection** -Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="7a3c4-116">Um zu testen, ob ein Medien Element ein Member einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabeliste mit *Player* ab. *playlistcollection*. **getByName**(*Name*). **Element**(0).</span><span class="sxs-lookup"><span data-stu-id="7a3c4-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="7a3c4-117">Diese Methode kann auch mit CD-und metadatenwiedergabe-Wiedergabelisten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="7a3c4-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7a3c4-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7a3c4-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7a3c4-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a3c4-120">Examples</span></span>

<span data-ttu-id="7a3c4-121">Im folgenden JScript-Beispiel werden *Medien* verwendet. **ismembership of** , um zu testen, ob das aktuelle Medien Element ein Member der Wiedergabeliste mit dem Namen "Beispiel Wiedergabeliste" ist.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="7a3c4-122">Wenn dies nicht der Fall ist, wird das aktuelle Medien Element an die Beispiel Wiedergabeliste angehängt.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="7a3c4-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="7a3c4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a3c4-124">Requirements</span></span>



| <span data-ttu-id="7a3c4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a3c4-125">Requirement</span></span> | <span data-ttu-id="7a3c4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3c4-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3c4-127">Version</span><span class="sxs-lookup"><span data-stu-id="7a3c4-127">Version</span></span><br/> | <span data-ttu-id="7a3c4-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7a3c4-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7a3c4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7a3c4-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a3c4-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a3c4-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a3c4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a3c4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a3c4-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="7a3c4-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7a3c4-133">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="7a3c4-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7a3c4-134">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7a3c4-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="7a3c4-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7a3c4-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7a3c4-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7a3c4-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





