---
title: Network.bufferingCount
description: Die bufferingCount-Eigenschaft ruft ab, wie oft die Pufferung während der Clipwiedergabe aufgetreten ist.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network.bufferingCount-Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d19c80715ca04965927bb0a50450213d707beeb124fd671fd8071e2cdd90e3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901760"
---
# <a name="networkbufferingcount"></a>Network.bufferingCount

Die **bufferingCount-Eigenschaft** ruft ab, wie oft die Pufferung während der Clipwiedergabe aufgetreten ist.

## <a name="syntax"></a>Syntax

*Player*. *network*. **bufferingCount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf 0 (null) festgelegt. Sie wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wird.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft gibt gültige Informationen nur zur Laufzeit zurück, wenn der *Player*. **Die URL-Eigenschaft** ist festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **bufferingCount,** um anzuzeigen, wie oft die Pufferung während der Wiedergabe auftritt. Die Informationen werden in einem HTML-DIV angezeigt, der mit der ID = "CB" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
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

 

 





