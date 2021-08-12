---
title: Network.empfangQuality
description: Die eigenschaft "empfangsqualität" ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden empfangen wurden.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Network.empfangQuality Windows Media Player
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
ms.openlocfilehash: 159bcac192d5a5bd9197ecc3ea935027dd6d707dde42a54c64a318459ae00040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574156"
---
# <a name="networkreceptionquality"></a>Network.empfangQuality

Die **eigenschaft "empfangsqualität"** ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden empfangen wurden.

## <a name="syntax"></a>Syntax

*Player*. *network*. **empfangQuality**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Die Anzahl der während des Streamings empfangenen, verlorenen und wiederhergestellten Pakete wird einmal pro Sekunde überwacht. **"packetQuality"** ist der Prozentsatz der Pakete, die in den letzten 30 Sekunden nicht verloren gegangen sind.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Diese Eigenschaft gibt gültige Informationen nur während der Laufzeit und nur dann zurück, wenn der *Player*. Die **URL-Eigenschaft** ist ebenfalls festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **empfangQualität,** um den Prozentsatz der empfangenen Pakete anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID " RQ" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 30 Sekunden verwendet, um die Anzeige zu aktualisieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





