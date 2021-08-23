---
title: Network.bandWidth
description: Die bandWidth-Eigenschaft ruft die aktuelle Bandbreite des Clips ab.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network.bandWidth Windows Media Player
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
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616877"
---
# <a name="networkbandwidth"></a>Network.bandWidth

Die **bandWidth-Eigenschaft** ruft die aktuelle Bandbreite des Clips ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **bandWidth**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt 0 (null) zurück, wenn *der Player*. **Die URL-Eigenschaft** ist nicht festgelegt. Diese Eigenschaft ist nur für Streamingmedien gültig.

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript beispiel wird Network *verwendet.* **bandWidth,** um die aktuelle Medienbandbreite anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, der mit der ID = "BW" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





