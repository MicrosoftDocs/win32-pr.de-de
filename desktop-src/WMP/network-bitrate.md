---
title: Network.bitRate
description: Die bitRate-Eigenschaft ruft die aktuelle empfangene Bitrate ab.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Network.bitRate-Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901780"
---
# <a name="networkbitrate"></a>Network.bitRate

Die **bitRate-Eigenschaft** ruft die aktuelle empfangene Bitrate ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **bitRate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Dieser Wert ist eine Kombination der Bitraten der aktuellen Video- und Audiostreams.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **bitRate** zum Anzeigen der aktuellen Medienbitrate. Die Informationen werden in einem HTML-DIV angezeigt, der mit der ID = "BR" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

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
</dt> </dl>

 

 





