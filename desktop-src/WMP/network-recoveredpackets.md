---
title: Network. Wiederherstellungspakete
description: Die Wiederherstellungs Pakete-Eigenschaft ruft die Anzahl der wiederhergestellten Pakete ab.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Netzwerk. Wiederherstellungspakete (Windows Media Player)
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368560"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="b8cfd-104">Network. Wiederherstellungspakete</span><span class="sxs-lookup"><span data-stu-id="b8cfd-104">Network.recoveredPackets</span></span>

<span data-ttu-id="b8cfd-105">Die **Wiederherstellungs Pakete** -Eigenschaft ruft die Anzahl der wiederhergestellten Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cfd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8cfd-106">Syntax</span></span>

<span data-ttu-id="b8cfd-107">*Player*. *Netzwerk*. wieder **herstellbare Pakete**</span><span class="sxs-lookup"><span data-stu-id="b8cfd-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b8cfd-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b8cfd-108">Possible Values</span></span>

<span data-ttu-id="b8cfd-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="b8cfd-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cfd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8cfd-110">Remarks</span></span>

<span data-ttu-id="b8cfd-111">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="b8cfd-112">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="b8cfd-113">Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="b8cfd-114">Sie entspricht 0 (null), wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="b8cfd-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8cfd-115">Examples</span></span>

<span data-ttu-id="b8cfd-116">Im folgenden JScript-Beispiel wird *Network* verwendet. **Wiederherstellungs Pakete** zum Anzeigen der Anzahl der wiederhergestellten Pakete.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="b8cfd-117">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "PR" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="b8cfd-118">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="b8cfd-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="b8cfd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8cfd-120">Requirements</span></span>



| <span data-ttu-id="b8cfd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8cfd-121">Requirement</span></span> | <span data-ttu-id="b8cfd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b8cfd-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cfd-123">Version</span><span class="sxs-lookup"><span data-stu-id="b8cfd-123">Version</span></span><br/> | <span data-ttu-id="b8cfd-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b8cfd-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b8cfd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cfd-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8cfd-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8cfd-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8cfd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8cfd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cfd-128">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="b8cfd-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="b8cfd-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="b8cfd-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





