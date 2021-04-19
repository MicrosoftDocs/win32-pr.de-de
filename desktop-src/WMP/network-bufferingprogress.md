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
# <a name="networkbufferingprogress"></a>Network. BufferingProgress

Die **BufferingProgress** -Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **BufferingProgress**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft gibt nur während der Laufzeit gültige Informationen zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.

Verwenden Sie das Ereignis *Player*. * * * * Buffering* * * *, um zu bestimmen, wann die Pufferung startet oder beendet wird.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **BufferingProgress** , um den Prozentsatz der abgeschlossenen Pufferung anzuzeigen. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "BP" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





