---
title: Network. Bitrate
description: Die Bitrate-Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Windows-Media Player "Network. Bitrate"
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
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370013"
---
# <a name="networkbitrate"></a>Network. Bitrate

Die **Bitrate** -Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **Bitrate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist eine Kombination aus den Bitraten der aktuellen Video-und Audiodatenströme.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **Bitrate** zum Anzeigen der aktuellen Medien Bitrate. Die Informationen werden in einem mit ID = "br" erstellten HTML-div angezeigt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





