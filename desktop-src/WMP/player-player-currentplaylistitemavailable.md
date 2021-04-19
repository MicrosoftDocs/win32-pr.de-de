---
title: Player. currentplaylistitemavailable-Ereignis
description: Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird. | Player. currentplaylistitemavailable-Ereignis
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Currentplaylistitemavailable-Ereignisfenster Media Player
- Currentplaylistitemavailable-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentplaylistitemavailable-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361291"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="91ed5-107">Player. currentplaylistitemavailable-Ereignis</span><span class="sxs-lookup"><span data-stu-id="91ed5-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="91ed5-108">Das **currentplaylistitemavailable** -Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="91ed5-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ed5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ed5-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="91ed5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91ed5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ed5-111">*bstritemname*</span><span class="sxs-lookup"><span data-stu-id="91ed5-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="91ed5-112">**Zeichenfolge** , die den Namen des aktuellen Wiedergabelisten Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="91ed5-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ed5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91ed5-113">Return value</span></span>

<span data-ttu-id="91ed5-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="91ed5-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ed5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91ed5-115">Remarks</span></span>

<span data-ttu-id="91ed5-116">Der Name der aktuellen Wiedergabeliste kann verwendet werden, um das entsprechende **Wiedergabe** Listen Objekt mithilfe von *playlistcollection* abzurufen. **getByName** -Methode.</span><span class="sxs-lookup"><span data-stu-id="91ed5-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="91ed5-117">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="91ed5-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="91ed5-118">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="91ed5-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="91ed5-119">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91ed5-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ed5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91ed5-120">Requirements</span></span>



| <span data-ttu-id="91ed5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91ed5-121">Requirement</span></span> | <span data-ttu-id="91ed5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="91ed5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91ed5-123">Version</span><span class="sxs-lookup"><span data-stu-id="91ed5-123">Version</span></span><br/> | <span data-ttu-id="91ed5-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="91ed5-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="91ed5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="91ed5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="91ed5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ed5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ed5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91ed5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ed5-128">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="91ed5-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="91ed5-129">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="91ed5-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="91ed5-130">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="91ed5-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





