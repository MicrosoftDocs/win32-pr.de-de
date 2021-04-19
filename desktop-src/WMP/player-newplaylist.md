---
title: Player. newwiedergabe-Methode
description: Die newwiedergabe-Methode erstellt ein neues Wiedergabelisten Objekt.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354035"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="89edc-106">Player. newwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="89edc-106">Player.newPlaylist method</span></span>

<span data-ttu-id="89edc-107">Die **newwiedergabe** -Methode erstellt ein neues **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="89edc-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="89edc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89edc-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="89edc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="89edc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89edc-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89edc-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89edc-111">**Zeichenfolge** , die den Namen der neuen Wiedergabeliste enthält.</span><span class="sxs-lookup"><span data-stu-id="89edc-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="89edc-112">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89edc-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89edc-113">**Zeichenfolge** , die die URL der Windows Media-Metadatei-Wiedergabeliste enthält, mit der das **Wiedergabe** Listen Objekt erstellt</span><span class="sxs-lookup"><span data-stu-id="89edc-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89edc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89edc-114">Return value</span></span>

<span data-ttu-id="89edc-115">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="89edc-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89edc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89edc-116">Remarks</span></span>

<span data-ttu-id="89edc-117">Wenn der *URL* -Parameter auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird ein leeres **Wiedergabe** Listen Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="89edc-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="89edc-118">Wenn der *Name* -Parameter auf "" festgelegt ist, wird der Name in der Metadatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="89edc-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="89edc-119">Die neue Wiedergabeliste, die mit dieser Methode erstellt wurde, wird nicht der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89edc-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="89edc-120">Verwenden Sie *playlistcollection*, um der Bibliothek eine neue Wiedergabeliste hinzuzufügen. **importwiedergabe Liste** oder *playlistcollection*. **newwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="89edc-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="89edc-121">Alle führenden oder nachfolgenden Leerzeichen im Wiedergabelisten Namen werden automatisch entfernt, wenn Sie der Bibliothek hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="89edc-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="89edc-122">Da die Bibliothek mehrere Wiedergabelisten mit dem gleichen Namen zulässt, sollten Sie überprüfen, ob eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist, bevor Sie einen neuen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89edc-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="89edc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89edc-123">Requirements</span></span>



| <span data-ttu-id="89edc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89edc-124">Requirement</span></span> | <span data-ttu-id="89edc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="89edc-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89edc-126">Version</span><span class="sxs-lookup"><span data-stu-id="89edc-126">Version</span></span><br/> | <span data-ttu-id="89edc-127">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89edc-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="89edc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="89edc-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="89edc-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89edc-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89edc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89edc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89edc-131">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="89edc-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="89edc-132">**Playlistcollection. importwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="89edc-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="89edc-133">**Playlistcollection. newwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="89edc-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="89edc-134">**Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="89edc-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





