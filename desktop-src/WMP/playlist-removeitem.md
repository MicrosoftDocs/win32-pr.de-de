---
title: Wiedergabe. RemoveItem-Methode
description: Die RemoveItem-Methode entfernt das angegebene Element aus der Wiedergabeliste.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- RemoveItem-Methode, Windows-Media Player
- RemoveItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, RemoveItem-Methode
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368411"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="0bfa4-106">Wiedergabe. RemoveItem-Methode</span><span class="sxs-lookup"><span data-stu-id="0bfa4-106">Playlist.removeItem method</span></span>

<span data-ttu-id="0bfa4-107">Die **RemoveItem** -Methode entfernt das angegebene Element aus der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bfa4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bfa4-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="0bfa4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bfa4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bfa4-110">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bfa4-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bfa4-111">Das zu entfernende **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bfa4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bfa4-112">Return value</span></span>

<span data-ttu-id="0bfa4-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bfa4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bfa4-114">Remarks</span></span>

<span data-ttu-id="0bfa4-115">, Wenn das entfernte Element die aktuell wiedergegebene Spur (*Player*) ist.**currentMedia**), Wiedergabe wird beendet, und das nächste Element in der Wiedergabeliste wird zum aktuellen Element.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="0bfa4-116">Wenn kein nächstes Element vorhanden ist, wird das vorherige Element verwendet, oder wenn keine anderen Elemente vorhanden sind, dann *Player*. **currentMedia** wird auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="0bfa4-117">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="0bfa4-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0bfa4-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bfa4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bfa4-119">Requirements</span></span>



| <span data-ttu-id="0bfa4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bfa4-120">Requirement</span></span> | <span data-ttu-id="0bfa4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0bfa4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfa4-122">Version</span><span class="sxs-lookup"><span data-stu-id="0bfa4-122">Version</span></span><br/> | <span data-ttu-id="0bfa4-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0bfa4-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0bfa4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0bfa4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bfa4-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bfa4-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bfa4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bfa4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bfa4-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="0bfa4-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0bfa4-129">**Wiedergabeliste. InsertItem**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="0bfa4-130">**Wiedergabeliste. Element**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="0bfa4-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0bfa4-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0bfa4-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





