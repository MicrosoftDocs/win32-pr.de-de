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
# <a name="networkreceptionquality"></a>Network. receptionquality

Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden empfangenen Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. " **receptionquality** "

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Die Anzahl der während des Streamings empfangenen, verlorenen und wiederhergestellten Pakete wird einmal pro Sekunde überwacht. " **receptionquality** " ist der Prozentsatz von Paketen, die während der letzten 30 Sekunden nicht verloren gegangen sind.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist ebenfalls festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. " **receptionquality** " zeigt den Prozentsatz der empfangenen Pakete an. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "RQ" erstellt wurde. Das Beispiel verwendet einen Timer mit einem Intervall von 30 Sekunden, um die Anzeige zu aktualisieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





