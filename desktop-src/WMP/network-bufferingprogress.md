---
title: Network. BufferingProgress
description: Die BufferingProgress-Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Network. BufferingProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369454"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="0a9bd-104">Network. BufferingProgress</span><span class="sxs-lookup"><span data-stu-id="0a9bd-104">Network.bufferingProgress</span></span>

<span data-ttu-id="0a9bd-105">Die **BufferingProgress** -Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a9bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a9bd-106">Syntax</span></span>

<span data-ttu-id="0a9bd-107">*Player*. *Netzwerk*. **BufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0a9bd-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0a9bd-108">Possible Values</span></span>

<span data-ttu-id="0a9bd-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9bd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a9bd-110">Remarks</span></span>

<span data-ttu-id="0a9bd-111">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="0a9bd-112">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="0a9bd-113">Die Pufferung gilt nur für Streaminginhalte.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="0a9bd-114">Diese Eigenschaft gibt nur während der Laufzeit gültige Informationen zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="0a9bd-115">Verwenden Sie das Ereignis *Player*. \* \* \* \* Buffering\* \* \* \*, um zu bestimmen, wann die Pufferung startet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="0a9bd-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a9bd-116">Examples</span></span>

<span data-ttu-id="0a9bd-117">Im folgenden JScript-Beispiel wird *Network* verwendet. **BufferingProgress** , um den Prozentsatz der abgeschlossenen Pufferung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="0a9bd-118">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "BP" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="0a9bd-119">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="0a9bd-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="0a9bd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a9bd-121">Requirements</span></span>



| <span data-ttu-id="0a9bd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a9bd-122">Requirement</span></span> | <span data-ttu-id="0a9bd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0a9bd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9bd-124">Version</span><span class="sxs-lookup"><span data-stu-id="0a9bd-124">Version</span></span><br/> | <span data-ttu-id="0a9bd-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0a9bd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0a9bd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a9bd-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9bd-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9bd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a9bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9bd-129">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="0a9bd-130">**Player. buffereing-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="0a9bd-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





