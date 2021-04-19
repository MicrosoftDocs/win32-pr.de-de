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
# <a name="networkdownloadprogress"></a>Network. Download Progress

Die **DownloadProgress** -Eigenschaft ruft den abgeschlossenen Prozentsatz des Downloads ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **Download Fortschritt**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Wenn das Windows Media Player-Steuerelement mit einer Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, gibt die **DownloadProgress** -Eigenschaft den Prozentsatz der gesamten heruntergeladenen Datei zurück. Diese Funktion wird zurzeit nur auf Webservern unterstützt. Die folgenden Dateiformate können gleichzeitig heruntergeladen und abgespielt werden:

-   Advanced Systems Format (ASF)
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)
-   MP3
-   MPEG
-   WAV
-   Einige AVI-Dateien

Verwenden Sie den *Player*. **Bufferingereignis** , um zu bestimmen, wann der Download beginnt und endet.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **Download Fortschritt** , um den Prozentsatz der abgeschlossenen Downloads anzuzeigen. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "DP" erstellt wurde. Das Beispiel verwendet einen Timer mit einem 1-Sekunden-Intervall, um die Anzeige zu aktualisieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player. buffereing-Ereignis**](player-player-buffering.md)
</dt> </dl>

 

 





