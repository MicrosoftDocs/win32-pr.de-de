---
title: Player. Currency Change-Ereignis
description: Das Ereignis "Ereignis Ereignisse" tritt auf, wenn sich "Controls. Events Item" ändert.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Ereignisfenster für das Ereignis Ereignis Media Player
- Ereignis für den Ereignis Wechsel in Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, Ereignis für den Ereignis Wechsel
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371319"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="a689b-106">Player. Currency Change-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a689b-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="a689b-107">Das **Ereignis** "Ereignis Ereignisse" tritt auf, wenn-Steuer *Elemente*. das Ereignis **wird geändert.**</span><span class="sxs-lookup"><span data-stu-id="a689b-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a689b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a689b-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="a689b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a689b-109">Parameters</span></span>

<span data-ttu-id="a689b-110">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="a689b-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a689b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a689b-111">Return value</span></span>

<span data-ttu-id="a689b-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a689b-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a689b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a689b-113">Examples</span></span>

<span data-ttu-id="a689b-114">Im folgenden JScript-Beispiel wird ein Ereignishandler für den *Player* veranschaulicht. Ereignis für die Ereignis Ereignis **Änderung** .</span><span class="sxs-lookup"><span data-stu-id="a689b-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="a689b-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a689b-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="a689b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a689b-116">Requirements</span></span>



| <span data-ttu-id="a689b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a689b-117">Requirement</span></span> | <span data-ttu-id="a689b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a689b-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a689b-119">Version</span><span class="sxs-lookup"><span data-stu-id="a689b-119">Version</span></span><br/> | <span data-ttu-id="a689b-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a689b-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a689b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a689b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a689b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a689b-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a689b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a689b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a689b-124">**Controls. happtitem**</span><span class="sxs-lookup"><span data-stu-id="a689b-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="a689b-125">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a689b-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





