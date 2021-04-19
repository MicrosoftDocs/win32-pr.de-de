---
title: Netzwerkbandbreite
description: Die Bandbreiten Eigenschaft ruft die aktuelle Bandbreite des Clips ab.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Netzwerk-Bandbreiten Fenster Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356382"
---
# <a name="networkbandwidth"></a>Netzwerkbandbreite

Die **Bandbreiten** Eigenschaft ruft die aktuelle Bandbreite des Clips ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **Bandbreite**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt NULL zurück, wenn der *Player*. Die **URL** -Eigenschaft ist nicht festgelegt. Diese Eigenschaft ist nur für Streamingmedien gültig.

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript-Beispiel wird *Network* verwendet. **Bandbreite** zum Anzeigen der aktuellen Medien Bandbreite. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "BW" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
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

 

 





