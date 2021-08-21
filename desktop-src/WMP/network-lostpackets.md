---
title: Network.lostPackets
description: Die lostPackets-Eigenschaft ruft die Anzahl verlorener Pakete ab.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network.lostPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f4c4211383095559c605de51fd5b182f53632272f268112fd6bdf6aef6dd718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836204"
---
# <a name="networklostpackets"></a>Network.lostPackets

Die **lostPackets-Eigenschaft** ruft die Anzahl verlorener Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **lostPackets**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur für Streamingmedien gültig und entspricht 0 (null), wenn das VERLUSTLOSE HTTP-Protokoll verwendet wird.

Pakete können aus einer Reihe von Gründen verloren gehen, z. B. dem Typ und der Qualität der Netzwerkverbindung.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten und neu gestartet wird. Diese Eigenschaft gibt gültige Informationen nur zur Laufzeit zurück, und nur, wenn der *Player*. **Die URL-Eigenschaft** ist festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **lostPackets,** um die Gesamtanzahl von Paketen anzuzeigen, die während der Wiedergabe verloren gegangen sind, wenn der Benutzer auf eine Schaltfläche klickt. Die Informationen werden in einem HTML-DIV angezeigt, der mit der ID = "LP" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





