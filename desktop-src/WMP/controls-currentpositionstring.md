---
title: Controls. currentpositionstring
description: Die currentpositionstring-Eigenschaft ruft die aktuelle Position im Medien Element als Zeichenfolge ab, die als hh mm SS (Stunden, Minuten und Sekunden) formatiert ist.
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls. currentpositionstring Windows Media Player
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
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371490"
---
# <a name="controlscurrentpositionstring"></a>Controls. currentpositionstring

Die **currentpositionstring** -Eigenschaft ruft die aktuelle Position im Medien Element als **Zeichen** Folge ab, die als hh: mm: SS (Stunden, Minuten und Sekunden) formatiert ist.

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Wenn das Medien Element weniger als eine Stunde lang ist, wird der HH:-Teil nicht eingeschlossen.

> [!Note]  
> Sie sollten Code einschließen, um den Timer zu beenden, wenn das Medien Element beendet oder angehalten wird.

 

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird ein HTML-Timer gestartet, der die aktuelle Position der Mediendatei in Intervallen von einer Sekunde anzeigt. Ein HTML-Textelement mit dem Namen MyText wurde erstellt, um die aktuelle Position anzuzeigen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 





