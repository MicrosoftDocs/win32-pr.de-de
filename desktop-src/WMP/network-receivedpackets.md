---
title: Network.receivedPackets
description: Die receivedPackets-Eigenschaft ruft die Anzahl der empfangenen Pakete ab.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network.receivedPackets Windows Media Player
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
ms.openlocfilehash: ca9544332fa6e81211dae45cddc74ce9daee0d47e70d467137aaca2084bbc6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054498"
---
# <a name="networkreceivedpackets"></a>Network.receivedPackets

Die **receivedPackets-Eigenschaft** ruft die Anzahl der empfangenen Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **receivedPackets**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Jedes Mal, wenn die Clipwiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Dateiwiedergabe angehalten wird.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **receivedPackets,** um die Anzahl der empfangenen Pakete anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID = "RP" erstellt wurde. Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





