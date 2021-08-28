---
title: Network.bufferingProgress
description: Die bufferingProgress-Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Network.bufferingProgress Windows Media Player
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
ms.openlocfilehash: 65de3f7b1b58dfb90f76436f324dcc3d4fc3fe9a24b7c60ca3db888771f9192d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901750"
---
# <a name="networkbufferingprogress"></a>Network.bufferingProgress

Die **bufferingProgress-Eigenschaft** ruft den Prozentsatz der abgeschlossenen Pufferung ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **bufferingProgress**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft gibt gültige Informationen nur während der Laufzeit zurück, wenn der *Player*. **Die URL-Eigenschaft** ist festgelegt.

Verwenden Sie das *Player-Ereignis*".**Buffering!", um zu bestimmen, wann die Pufferung gestartet oder beendet wird.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **bufferingProgress,** um den Prozentsatz der abgeschlossenen Pufferung anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID " BP" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.Buffering-Ereignis**](player-player-buffering.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





