---
title: Network. bufferingcount
description: Die bufferingcount-Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Clip Wiedergabe erfolgt ist.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network. bufferingcount-Windows-Media Player
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
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370012"
---
# <a name="networkbufferingcount"></a>Network. bufferingcount

Die **bufferingcount** -Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Clip Wiedergabe erfolgt ist.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **bufferingcount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt. Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.

Die Pufferung gilt nur für Streaminginhalte. Diese Eigenschaft gibt gültige Informationen nur zur Laufzeit zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **bufferingcount** , um anzuzeigen, wie oft die Pufferung während der Wiedergabe auftritt. Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "CB" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





