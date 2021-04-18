---
title: Network. receptionquality
description: Die Eigenschaft "receptionquality" Ruft den Prozentsatz der in den letzten 30 Sekunden empfangenen Pakete ab.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Network. receptionquality-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358704"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="c0e4a-104">Network. receptionquality</span><span class="sxs-lookup"><span data-stu-id="c0e4a-104">Network.receptionQuality</span></span>

<span data-ttu-id="c0e4a-105">Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e4a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0e4a-106">Syntax</span></span>

<span data-ttu-id="c0e4a-107">*Player*. *Netzwerk*. " **receptionquality** "</span><span class="sxs-lookup"><span data-stu-id="c0e4a-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c0e4a-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c0e4a-108">Possible Values</span></span>

<span data-ttu-id="c0e4a-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c0e4a-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e4a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0e4a-110">Remarks</span></span>

<span data-ttu-id="c0e4a-111">Die Anzahl der während des Streamings empfangenen, verlorenen und wiederhergestellten Pakete wird einmal pro Sekunde überwacht.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="c0e4a-112">" **receptionquality** " ist der Prozentsatz von Paketen, die während der letzten 30 Sekunden nicht verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="c0e4a-113">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="c0e4a-114">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="c0e4a-115">Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="c0e4a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0e4a-116">Examples</span></span>

<span data-ttu-id="c0e4a-117">Im folgenden JScript-Beispiel wird *Network* verwendet. " **receptionquality** " zeigt den Prozentsatz der empfangenen Pakete an.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="c0e4a-118">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "RQ" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="c0e4a-119">Das Beispiel verwendet einen Timer mit einem Intervall von 30 Sekunden, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="c0e4a-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c0e4a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0e4a-121">Requirements</span></span>



| <span data-ttu-id="c0e4a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0e4a-122">Requirement</span></span> | <span data-ttu-id="c0e4a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c0e4a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e4a-124">Version</span><span class="sxs-lookup"><span data-stu-id="c0e4a-124">Version</span></span><br/> | <span data-ttu-id="c0e4a-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c0e4a-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c0e4a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e4a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0e4a-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0e4a-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e4a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0e4a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e4a-129">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="c0e4a-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c0e4a-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="c0e4a-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





