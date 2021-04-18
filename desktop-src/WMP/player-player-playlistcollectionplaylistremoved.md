---
title: Player. playlistcollectionplaylistreverschogereignis
description: Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird. | Player. playlistcollectionplaylistreverschogereignis
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player "playlistcollectionplaylistreverschoder Ereignisfenster"
- Playlistcollectionplaylistregerührt-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistcollectionplaylistreverschoeignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371528"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="228b1-107">Player. playlistcollectionplaylistreverschogereignis</span><span class="sxs-lookup"><span data-stu-id="228b1-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="228b1-108">Das **playlistcollectionplaylistrebewegungs-Ereignis** tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="228b1-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="228b1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="228b1-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="228b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="228b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228b1-111">*bstrauplaylistname*</span><span class="sxs-lookup"><span data-stu-id="228b1-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="228b1-112">Eine **Zeichenfolge** , die den Namen der entfernten Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="228b1-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="228b1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="228b1-113">Return value</span></span>

<span data-ttu-id="228b1-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="228b1-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="228b1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="228b1-115">Remarks</span></span>

<span data-ttu-id="228b1-116">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="228b1-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="228b1-117">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="228b1-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="228b1-118">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="228b1-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="228b1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="228b1-119">Requirements</span></span>



| <span data-ttu-id="228b1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="228b1-120">Requirement</span></span> | <span data-ttu-id="228b1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="228b1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="228b1-122">Version</span><span class="sxs-lookup"><span data-stu-id="228b1-122">Version</span></span><br/> | <span data-ttu-id="228b1-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="228b1-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="228b1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="228b1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="228b1-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="228b1-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228b1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="228b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228b1-127">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="228b1-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="228b1-128">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="228b1-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





