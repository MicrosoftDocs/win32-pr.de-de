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
# <a name="networkreceivedpackets"></a>Network. receivedpakete

Die **receivedpaketen** -Eigenschaft ruft die Anzahl der empfangenen Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **receivedpakete**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Clip Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Dateiwiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **receivedpakete** zum Anzeigen der Anzahl empfangener Pakete. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "RP" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





