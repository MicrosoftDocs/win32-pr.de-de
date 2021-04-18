---
title: Controls. happtitem
description: Die Eigenschaft "ustitem" gibt das aktuelle Medien Element an oder ruft es ab.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Steuerelemente. Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361349"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="6ea36-104">Controls. happtitem</span><span class="sxs-lookup"><span data-stu-id="6ea36-104">Controls.currentItem</span></span>

<span data-ttu-id="6ea36-105">Die Eigenschaft " **ustitem** " gibt das aktuelle Medien Element an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="6ea36-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="6ea36-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="6ea36-106">Possible Values</span></span>

<span data-ttu-id="6ea36-107">Diese Eigenschaft ist ein **Medien** Objekt mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6ea36-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea36-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ea36-108">Remarks</span></span>

<span data-ttu-id="6ea36-109">Diese Methode funktioniert nur mit Elementen in *Player*. **currentwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="6ea36-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="6ea36-110">Das Aufrufen von " **happtitem** " mit einem Verweis auf ein gespeichertes Medien Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ea36-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6ea36-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ea36-111">Examples</span></span>

<span data-ttu-id="6ea36-112">Im folgenden JScript-Beispiel wird das Steuer **Element für das** Player-Steuerelement in einem HTML-SELECT-Element auf den ausgewählten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ea36-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="6ea36-113">Die aktuelle Wiedergabeliste wurde zuerst mithilfe von *playlistcollection* angegeben. **getByName**.</span><span class="sxs-lookup"><span data-stu-id="6ea36-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="6ea36-114">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6ea36-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6ea36-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ea36-115">Requirements</span></span>



| <span data-ttu-id="6ea36-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ea36-116">Requirement</span></span> | <span data-ttu-id="6ea36-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6ea36-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea36-118">Version</span><span class="sxs-lookup"><span data-stu-id="6ea36-118">Version</span></span><br/> | <span data-ttu-id="6ea36-119">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6ea36-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6ea36-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea36-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ea36-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea36-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ea36-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea36-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea36-123">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="6ea36-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6ea36-124">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="6ea36-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6ea36-125">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="6ea36-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





