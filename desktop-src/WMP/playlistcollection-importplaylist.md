---
title: Playlistcollection. importwiedergabe-Methode
description: Die importwiedergabe-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | Playlistcollection. importwiedergabe-Methode
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- importwiedergabe-Methode, Windows-Media Player
- importwiedergabe-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, importwiedergabe-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351376"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="b3056-107">Playlistcollection. importwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="b3056-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="b3056-108">Die **importwiedergabe** -Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3056-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3056-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3056-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="b3056-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3056-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3056-111">*Wiedergabeliste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3056-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3056-112">Das hinzu zufügende **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3056-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3056-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3056-113">Return value</span></span>

<span data-ttu-id="b3056-114">Diese Methode gibt das **Wiedergabe** Listen Objekt zurück, das hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b3056-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3056-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3056-115">Remarks</span></span>

<span data-ttu-id="b3056-116">Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek nicht mithilfe dieser Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b3056-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="b3056-117">Verwenden Sie die **newwiedergabe** -Methode, um eine leere Wiedergabeliste in der Bibliothek zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3056-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="b3056-118">Anschließend können Sie die resultierende Wiedergabeliste mithilfe von *Wiedergabe* Listen mit Medien Elementen ausfüllen. **appendItem** oder *Wiedergabeliste*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="b3056-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="b3056-119">Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b3056-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="b3056-120">Wenn Sie der Bibliothek eine automatische Wiedergabeliste hinzufügen und das automatische Verhalten beibehalten möchten, verwenden Sie *mediacollection*. **fügen Sie hinzu**.</span><span class="sxs-lookup"><span data-stu-id="b3056-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="b3056-121">Weitere Informationen finden Sie unter [statische und automatische Wiedergabelisten](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="b3056-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="b3056-122">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3056-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b3056-123">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b3056-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3056-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3056-124">Requirements</span></span>



| <span data-ttu-id="b3056-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3056-125">Requirement</span></span> | <span data-ttu-id="b3056-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b3056-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3056-127">Version</span><span class="sxs-lookup"><span data-stu-id="b3056-127">Version</span></span><br/> | <span data-ttu-id="b3056-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b3056-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3056-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b3056-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3056-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3056-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3056-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3056-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3056-132">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="b3056-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="b3056-133">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b3056-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b3056-134">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="b3056-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="b3056-135">**Wiedergabeliste. appendItem**</span><span class="sxs-lookup"><span data-stu-id="b3056-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="b3056-136">**Wiedergabeliste. InsertItem**</span><span class="sxs-lookup"><span data-stu-id="b3056-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="b3056-137">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b3056-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="b3056-138">**Playlistcollection. newwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="b3056-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="b3056-139">**Playlistcollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="b3056-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="b3056-140">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="b3056-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b3056-141">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="b3056-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





