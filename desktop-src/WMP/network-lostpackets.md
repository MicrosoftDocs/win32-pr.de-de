---
title: Network. lostpakete
description: Die lostpaketen-Eigenschaft ruft die Anzahl der verlorenen Pakete ab.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network. lostpackt-Fenster Media Player
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
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364720"
---
# <a name="networklostpackets"></a>Network. lostpakete

Die **lostpaketen** -Eigenschaft ruft die Anzahl der verlorenen Pakete ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **lostpakete**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur für Streamingmedien gültig und gleich 0 (null), wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.

Pakete können aus verschiedenen Gründen verloren gehen, z. b. Art und Qualität der Netzwerkverbindung.

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Wiedergabe angehalten und neu gestartet wird, wird Sie nicht zurückgesetzt. Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **lostpakete** zum Anzeigen der Gesamtanzahl der Pakete, die während der Wiedergabe verloren gehen, wenn der Benutzer auf eine Schaltfläche klickt. Die Informationen werden in einem HTML div-Format angezeigt, das mit ID = "LP" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





