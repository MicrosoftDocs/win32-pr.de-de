---
title: Controls. PlayItem-Methode
description: Die PlayItem-Methode gibt das angegebene Medien Element wieder. | Controls. PlayItem-Methode
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- PlayItem-Methoden Fenster Media Player
- PlayItem-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, PlayItem-Methode
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366859"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="0309f-107">Controls. PlayItem-Methode</span><span class="sxs-lookup"><span data-stu-id="0309f-107">Controls.playItem method</span></span>

<span data-ttu-id="0309f-108">Die **PlayItem** -Methode gibt das angegebene Medien Element wieder.</span><span class="sxs-lookup"><span data-stu-id="0309f-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0309f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0309f-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="0309f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0309f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0309f-111">Das *mediaitem* \[ -Element in\]</span><span class="sxs-lookup"><span data-stu-id="0309f-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0309f-112">Das zu Wiedergabe Ende **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="0309f-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0309f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0309f-113">Return value</span></span>

<span data-ttu-id="0309f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0309f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0309f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0309f-115">Remarks</span></span>

<span data-ttu-id="0309f-116">Das Medien Element wird unabhängig vom Wert der *Einstellungen* geladen und automatisch wiedergegeben. **Autostart** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0309f-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="0309f-117">Wenn Sie ein Element ohne automatische Wiedergabe laden möchten, legen Sie die *Einstellungen* fest. **Autostart** mit false und Zuweisen eines Werts zu einem *Player*. Die **URL**, nach der **Play** aufgerufen werden kann, um mit der Wiedergabe des Elements zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="0309f-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="0309f-118">Hinweis</span><span class="sxs-lookup"><span data-stu-id="0309f-118">Note</span></span>

<span data-ttu-id="0309f-119">**PlayItem** funktioniert nur mit Elementen in *currentwiedergabe*.</span><span class="sxs-lookup"><span data-stu-id="0309f-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="0309f-120">Das Aufrufen von **PlayItem** mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0309f-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="0309f-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0309f-121">Examples</span></span>

<span data-ttu-id="0309f-122">Im folgenden JScript-Beispiel wird **PlayItem** verwendet, um ein Medien Element aus der aktuellen Wiedergabeliste wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="0309f-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="0309f-123">Das Element, das abgespielt werden soll, wird basierend auf seiner Position in der Wiedergabeliste ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0309f-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="0309f-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0309f-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="0309f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0309f-125">Requirements</span></span>



| <span data-ttu-id="0309f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0309f-126">Requirement</span></span> | <span data-ttu-id="0309f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0309f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0309f-128">Version</span><span class="sxs-lookup"><span data-stu-id="0309f-128">Version</span></span><br/> | <span data-ttu-id="0309f-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0309f-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0309f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0309f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0309f-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0309f-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0309f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0309f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0309f-133">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0309f-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0309f-134">**Wiedergabeliste. Element**</span><span class="sxs-lookup"><span data-stu-id="0309f-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





