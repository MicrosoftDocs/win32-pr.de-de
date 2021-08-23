---
title: Controls.currentPositionString
description: Die currentPositionString-Eigenschaft ruft die aktuelle Position im Medienelement als Zeichenfolge ab, die als HH MM SS formatiert ist (Stunden, Minuten und Sekunden).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls.currentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640f0f97e3fa4c4054df17ea92304ad7721c770d9cb9b56436dcf810b9c083ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651990"
---
# <a name="controlscurrentpositionstring"></a>Controls.currentPositionString

Die **currentPositionString-Eigenschaft** ruft die aktuelle Position im Medienelement als **Zeichenfolge** ab, die als HH:MM:SS formatiert ist (Stunden, Minuten und Sekunden).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="remarks"></a>Hinweise

Wenn das Medienelement weniger als eine Stunde lang ist, ist der Teil HH: nicht enthalten.

> [!Note]  
> Sie sollten Code einfügen, um den Timer zu beenden, wenn das Medienelement beendet oder angehalten wird.

 

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird ein HTML-Timer gestartet, der die aktuelle Position der Mediendatei in Intervallen von einer Sekunde anzeigt. Ein HTML TEXT-Element mit dem Namen MyText wurde erstellt, um die aktuelle Position anzuzeigen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





