---
title: Network.downloadProgress
description: Die downloadProgress-Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network.downloadProgress Windows Media Player
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
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901720"
---
# <a name="networkdownloadprogress"></a>Network.downloadProgress

Die **downloadProgress-Eigenschaft** ruft den Prozentsatz des abgeschlossenen Downloads ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **downloadProgress**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Wenn das Windows Media Player-Steuerelement mit einer Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, gibt die **downloadProgress-Eigenschaft** den Prozentsatz der gesamten heruntergeladenen Datei zurück. Dieses Feature wird derzeit nur auf Webservern unterstützt. Die folgenden Dateiformate können heruntergeladen und gleichzeitig abgespielt werden:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   Mpeg
-   WAV
-   Einige AVI-Dateien

Verwenden Sie *den Player*. **Pufferungsereignis,** um zu bestimmen, wann der Download beginnt und endet.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **downloadProgress, um** den Prozentsatz des abgeschlossenen Downloads anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, der mit der ID = "DP" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.Buffering-Ereignis**](player-player-buffering.md)
</dt> </dl>

 

 





