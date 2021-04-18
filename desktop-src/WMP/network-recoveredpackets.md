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
# <a name="networkrecoveredpackets"></a>Network. Wiederherstellungspakete

Die **Wiederherstellungs Pakete** -Eigenschaft ruft die Anzahl der wiederhergestellten Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. wieder **herstellbare Pakete**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist ebenfalls festgelegt. Sie entspricht 0 (null), wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **Wiederherstellungs Pakete** zum Anzeigen der Anzahl der wiederhergestellten Pakete. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "PR" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





