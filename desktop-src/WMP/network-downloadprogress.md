---
title: Network. Download Progress
description: Die DownloadProgress-Eigenschaft ruft den abgeschlossenen Prozentsatz des Downloads ab.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network. DownloadProgress-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373673"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="00455-104">Network. Download Progress</span><span class="sxs-lookup"><span data-stu-id="00455-104">Network.downloadProgress</span></span>

<span data-ttu-id="00455-105">Die **DownloadProgress** -Eigenschaft ruft den abgeschlossenen Prozentsatz des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="00455-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="00455-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="00455-106">Syntax</span></span>

<span data-ttu-id="00455-107">*Player*. *Netzwerk*. **Download Fortschritt**</span><span class="sxs-lookup"><span data-stu-id="00455-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="00455-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="00455-108">Possible Values</span></span>

<span data-ttu-id="00455-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="00455-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="00455-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00455-110">Remarks</span></span>

<span data-ttu-id="00455-111">Wenn das Windows Media Player-Steuerelement mit einer Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, gibt die **DownloadProgress** -Eigenschaft den Prozentsatz der gesamten heruntergeladenen Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="00455-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="00455-112">Diese Funktion wird zurzeit nur auf Webservern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00455-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="00455-113">Die folgenden Dateiformate können gleichzeitig heruntergeladen und abgespielt werden:</span><span class="sxs-lookup"><span data-stu-id="00455-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="00455-114">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="00455-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="00455-115">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="00455-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="00455-116">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="00455-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="00455-117">MP3</span><span class="sxs-lookup"><span data-stu-id="00455-117">MP3</span></span>
-   <span data-ttu-id="00455-118">MPEG</span><span class="sxs-lookup"><span data-stu-id="00455-118">MPEG</span></span>
-   <span data-ttu-id="00455-119">WAV</span><span class="sxs-lookup"><span data-stu-id="00455-119">WAV</span></span>
-   <span data-ttu-id="00455-120">Einige AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="00455-120">Some AVI files</span></span>

<span data-ttu-id="00455-121">Verwenden Sie den *Player*. **Bufferingereignis** , um zu bestimmen, wann der Download beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="00455-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="00455-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00455-122">Examples</span></span>

<span data-ttu-id="00455-123">Im folgenden JScript-Beispiel wird *Network* verwendet. **Download Fortschritt** , um den Prozentsatz der abgeschlossenen Downloads anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00455-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="00455-124">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "DP" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="00455-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="00455-125">Das Beispiel verwendet einen Timer mit einem 1-Sekunden-Intervall, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="00455-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="00455-126">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="00455-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="00455-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00455-127">Requirements</span></span>



| <span data-ttu-id="00455-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00455-128">Requirement</span></span> | <span data-ttu-id="00455-129">Wert</span><span class="sxs-lookup"><span data-stu-id="00455-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00455-130">Version</span><span class="sxs-lookup"><span data-stu-id="00455-130">Version</span></span><br/> | <span data-ttu-id="00455-131">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="00455-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="00455-132">DLL</span><span class="sxs-lookup"><span data-stu-id="00455-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="00455-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00455-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00455-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00455-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00455-135">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="00455-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="00455-136">**Player. buffereing-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="00455-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





