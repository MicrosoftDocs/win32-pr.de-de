---
title: Player. currentwiedergabe
description: Die currentwiedergabe-Eigenschaft gibt das aktuelle Wiedergabelisten Objekt an oder ruft es ab.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player. currentwiedergabe-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367742"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="0f341-104">Player. currentwiedergabe</span><span class="sxs-lookup"><span data-stu-id="0f341-104">Player.currentPlaylist</span></span>

<span data-ttu-id="0f341-105">Die currentwiedergabe-Eigenschaft gibt das aktuelle **Wiedergabe** Listen Objekt an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="0f341-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f341-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f341-106">Syntax</span></span>

<span data-ttu-id="0f341-107">*Player* . **currentwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="0f341-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0f341-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0f341-108">Possible Values</span></span>

<span data-ttu-id="0f341-109">Diese Eigenschaft ist ein Lese-/Schreib-Wiedergabe Listen Objekt. </span><span class="sxs-lookup"><span data-stu-id="0f341-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f341-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f341-110">Remarks</span></span>

<span data-ttu-id="0f341-111">Wenn die *Einstellungen*. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentwiedergabe** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f341-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="0f341-112">Diese Eigenschaft nimmt ein Wiedergabelisten Objekt an, das auf verschiedene Weise abgerufen werden kann, z. b. durch Aufrufen von *playlistarray*. **Item** oder *playlistcollection*. **newwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="0f341-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="0f341-113">Wenn Sie ein **Wiedergabe** Listenelement mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest oder verwenden *Player*. **newwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="0f341-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="0f341-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f341-114">Examples</span></span>

<span data-ttu-id="0f341-115">Im folgenden JScript-Beispiel wird die erste Wiedergabeliste in der-Bibliothek abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f341-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="0f341-116">Anschließend wird **currentwiedergabe** verwendet, um die abgerufene Wiedergabeliste zur aktuellen Wiedergabeliste zu machen, und dann, um den Namen der aktuellen Wiedergabeliste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0f341-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="0f341-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f341-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="0f341-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f341-118">Requirements</span></span>



| <span data-ttu-id="0f341-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f341-119">Requirement</span></span> | <span data-ttu-id="0f341-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0f341-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f341-121">Version</span><span class="sxs-lookup"><span data-stu-id="0f341-121">Version</span></span><br/> | <span data-ttu-id="0f341-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0f341-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0f341-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0f341-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f341-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f341-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f341-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f341-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f341-126">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f341-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0f341-127">**Player. newwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="0f341-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="0f341-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f341-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0f341-129">**Playlistarray. Item**</span><span class="sxs-lookup"><span data-stu-id="0f341-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="0f341-130">**Playlistcollection. newwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="0f341-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="0f341-131">**Einstellungen. Autostart**</span><span class="sxs-lookup"><span data-stu-id="0f341-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





