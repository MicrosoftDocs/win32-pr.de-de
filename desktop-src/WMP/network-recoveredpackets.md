---
title: Network.recoveredPackets
description: Die recoveredPackets-Eigenschaft ruft die Anzahl der wiederhergestellten Pakete ab.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Network.recoveredPackets Windows Media Player
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
ms.openlocfilehash: 464f7ad27603e506632d87254eaa4f76cbedf39ed15e353050cd13da0fa46204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134933"
---
# <a name="networkrecoveredpackets"></a>Network.recoveredPackets

Die **recoveredPackets-Eigenschaft** ruft die Anzahl der wiederhergestellten Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **recoveredPackets**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Diese Eigenschaft gibt gültige Informationen nur während der Laufzeit und nur dann zurück, wenn der *Player*. Die **URL-Eigenschaft** ist ebenfalls festgelegt. Bei Verwendung des HTTP-Protokolls, das verlustfrei ist, entspricht sie 0 (null).

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **recoveredPackets,** um die Anzahl der wiederhergestellten Pakete anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID " PR" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





