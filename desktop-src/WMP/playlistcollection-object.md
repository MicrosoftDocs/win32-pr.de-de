---
title: Playlistcollection-Objekt
description: Das playlistcollection-Objekt bietet eine Möglichkeit zum Organisieren von Wiedergabelisten.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Playlistcollection-Objekt, Windows-Media Player
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339244"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="f6f7f-104">Playlistcollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="f6f7f-104">PlaylistCollection Object</span></span>

<span data-ttu-id="f6f7f-105">Das **playlistcollection** -Objekt bietet eine Möglichkeit zum Organisieren von Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="f6f7f-106">Das **playlistcollection** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="f6f7f-107">Methode</span><span class="sxs-lookup"><span data-stu-id="f6f7f-107">Method</span></span>                                                  | <span data-ttu-id="f6f7f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6f7f-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6f7f-109">"GetAll"</span><span class="sxs-lookup"><span data-stu-id="f6f7f-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="f6f7f-110">Ruft ein [playlistarray](playlistarray-object.md) -Objekt ab, das alle Wiedergabelisten in der Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="f6f7f-111">getByName</span><span class="sxs-lookup"><span data-stu-id="f6f7f-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="f6f7f-112">Ruft ein [playlistarray](playlistarray-object.md) -Objekt ab, das ggf. vorhandene Wiedergabelisten mit dem angegebenen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="f6f7f-113">importwiedergabe Liste</span><span class="sxs-lookup"><span data-stu-id="f6f7f-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="f6f7f-114">Fügt der Bibliothek eine statische Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="f6f7f-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="f6f7f-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="f6f7f-116">Ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="f6f7f-117">neue</span><span class="sxs-lookup"><span data-stu-id="f6f7f-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="f6f7f-118">Erstellt eine neue Wiedergabeliste in der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="f6f7f-119">remove</span><span class="sxs-lookup"><span data-stu-id="f6f7f-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="f6f7f-120">Entfernt eine Wiedergabeliste aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="f6f7f-121">SetDeleted</span><span class="sxs-lookup"><span data-stu-id="f6f7f-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="f6f7f-122">Verschiebt eine Wiedergabeliste in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="f6f7f-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="f6f7f-123">Der Zugriff auf das **playlistcollection** -Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f6f7f-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="f6f7f-124">Object</span><span class="sxs-lookup"><span data-stu-id="f6f7f-124">Object</span></span>                      | <span data-ttu-id="f6f7f-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6f7f-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="f6f7f-126">Player</span><span class="sxs-lookup"><span data-stu-id="f6f7f-126">Player</span></span>](player-object.md) | [<span data-ttu-id="f6f7f-127">playlistcollection</span><span class="sxs-lookup"><span data-stu-id="f6f7f-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="f6f7f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6f7f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f7f-129">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="f6f7f-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




