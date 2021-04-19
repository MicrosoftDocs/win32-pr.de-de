---
title: Player. currentplaylistchange-Ereignis
description: Das currentplaylistchange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert. | Player. currentplaylistchange-Ereignis
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Currentplaylistchange-Ereignisfenster Media Player
- Currentplaylistchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentplaylistchange-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367615"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="7aaa9-107">Player. currentplaylistchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7aaa9-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="7aaa9-108">Das **currentplaylistchange** -Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aaa9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aaa9-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="7aaa9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aaa9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aaa9-111">*change*</span><span class="sxs-lookup"><span data-stu-id="7aaa9-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="7aaa9-112">**Zahl** (**Long**), die angibt, welche Art von Änderung in der Wiedergabeliste aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="7aaa9-113">Siehe den *Player*. **Playlistchange** -Ereignis für eine Tabelle mit möglichen Werten.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aaa9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7aaa9-114">Return value</span></span>

<span data-ttu-id="7aaa9-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aaa9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aaa9-116">Remarks</span></span>

<span data-ttu-id="7aaa9-117">Dieses Ereignis tritt nicht auf, wenn eine andere Wiedergabeliste zur aktuellen Wiedergabeliste wird.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="7aaa9-118">Sie tritt nur auf, wenn eine Änderung innerhalb der aktuellen Wiedergabeliste erfolgt, z. b. ein Medien Element, das an die Wiedergabeliste angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="7aaa9-119">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="7aaa9-120">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="7aaa9-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7aaa9-121">Examples</span></span>

<span data-ttu-id="7aaa9-122">Im folgenden JScript-Beispiel wird der Text in einem HTML div-Element mit dem Namen "plitems" aktualisiert, um die Namen der Medienelemente in der aktuellen Wiedergabeliste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="7aaa9-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="7aaa9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aaa9-124">Requirements</span></span>



| <span data-ttu-id="7aaa9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aaa9-125">Requirement</span></span> | <span data-ttu-id="7aaa9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7aaa9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7aaa9-127">Version</span><span class="sxs-lookup"><span data-stu-id="7aaa9-127">Version</span></span><br/> | <span data-ttu-id="7aaa9-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7aaa9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7aaa9-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7aaa9-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aaa9-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aaa9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aaa9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aaa9-132">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7aaa9-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7aaa9-133">**Player. currentwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="7aaa9-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="7aaa9-134">**Player. playlistchange**</span><span class="sxs-lookup"><span data-stu-id="7aaa9-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





