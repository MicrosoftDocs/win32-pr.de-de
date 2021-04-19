---
title: Network. sourceprotocol
description: Die sourceprotocol-Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network. sourceprotocol-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370617"
---
# <a name="networksourceprotocol"></a>Network. sourceprotocol

Die **sourceprotocol** -Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **sourceprotocol**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird auf "" (leere Zeichenfolge) festgelegt, wenn Medien von einer CD oder DVD abgespielt werden.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **sourceprotocol** zum Anzeigen des Quell Protokolls, das zum Empfangen von Daten verwendet wird. Die Informationen werden in einem mit ID = "SP" erstellten HTML-div angezeigt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
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

 

 





