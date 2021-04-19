---
title: Player. playlistcollectionplaylistadded-Ereignis
description: Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird. | Player. playlistcollectionplaylistadded-Ereignis
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Playlistcollectionplaylistadded-Ereignisfenster Media Player
- Playlistcollectionplaylistadded-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistcollectionplaylistadded-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366730"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="dce27-107">Player. playlistcollectionplaylistadded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="dce27-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="dce27-108">Das **playlistcollectionplaylistadded** -Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dce27-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce27-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce27-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="dce27-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dce27-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce27-111">*bstrauplaylistname*</span><span class="sxs-lookup"><span data-stu-id="dce27-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="dce27-112">Eine **Zeichenfolge** , die den Namen der hinzugefügten Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="dce27-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce27-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dce27-113">Return value</span></span>

<span data-ttu-id="dce27-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dce27-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce27-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dce27-115">Remarks</span></span>

<span data-ttu-id="dce27-116">Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um das entsprechende **Wiedergabe** Listen Objekt mithilfe von *playlistcollection* abzurufen. **getByName** -Methode.</span><span class="sxs-lookup"><span data-stu-id="dce27-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="dce27-117">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="dce27-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="dce27-118">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="dce27-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="dce27-119">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dce27-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce27-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce27-120">Requirements</span></span>



| <span data-ttu-id="dce27-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dce27-121">Requirement</span></span> | <span data-ttu-id="dce27-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dce27-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dce27-123">Version</span><span class="sxs-lookup"><span data-stu-id="dce27-123">Version</span></span><br/> | <span data-ttu-id="dce27-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="dce27-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dce27-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dce27-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dce27-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dce27-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce27-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dce27-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce27-128">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="dce27-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="dce27-129">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="dce27-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





