---
title: Network. receivedpakete
description: Die receivedpaketen-Eigenschaft ruft die Anzahl der empfangenen Pakete ab.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network. receivedpaketen-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362053"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="11582-104">Network. receivedpakete</span><span class="sxs-lookup"><span data-stu-id="11582-104">Network.receivedPackets</span></span>

<span data-ttu-id="11582-105">Die **receivedpaketen** -Eigenschaft ruft die Anzahl der empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="11582-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="11582-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11582-106">Syntax</span></span>

<span data-ttu-id="11582-107">*Player*. *Netzwerk*. **receivedpakete**</span><span class="sxs-lookup"><span data-stu-id="11582-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="11582-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="11582-108">Possible Values</span></span>

<span data-ttu-id="11582-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="11582-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="11582-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11582-110">Remarks</span></span>

<span data-ttu-id="11582-111">Jedes Mal, wenn die Clip Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11582-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="11582-112">Wenn die Dateiwiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="11582-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="11582-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11582-113">Examples</span></span>

<span data-ttu-id="11582-114">Im folgenden JScript-Beispiel wird *Network* verwendet. **receivedpakete** zum Anzeigen der Anzahl empfangener Pakete.</span><span class="sxs-lookup"><span data-stu-id="11582-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="11582-115">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "RP" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="11582-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="11582-116">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="11582-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="11582-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="11582-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="11582-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11582-118">Requirements</span></span>



| <span data-ttu-id="11582-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11582-119">Requirement</span></span> | <span data-ttu-id="11582-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11582-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11582-121">Version</span><span class="sxs-lookup"><span data-stu-id="11582-121">Version</span></span><br/> | <span data-ttu-id="11582-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="11582-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="11582-123">DLL</span><span class="sxs-lookup"><span data-stu-id="11582-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="11582-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11582-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11582-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11582-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11582-126">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="11582-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





