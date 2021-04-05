---
title: /cstruct_out Schalter
description: Der Schalter/cstruct_out ändert die C-Definition einer COM-Schnittstelle, die Strukturen zurückgibt, die mit der von a C++ Implementierer bereitgestellten ABI zu vergleichen sind.
keywords:
- /cstruct_out-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859361"
---
# <a name="cstruct_out-switch"></a>/cstruct \_ out-Schalter

Dieser Schalter ändert die C-Definition einer COM-Schnittstelle, die Strukturen zurückgibt, die mit der von a C++ Implementierer bereitgestellten ABI identisch sind.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Einige Schnittstellendefinitionen (insbesondere in `d3d12.idl` ) enthalten `__stdcall` Methoden, die Strukturen zurückgeben. C und C++ ABIS from MSVC unterscheiden sich in der Implementierung solcher Funktionen:

* C behandelt Sie als einfache Funktionen, die einen verborgenen `this` Zeiger als ersten Parameter verwenden. Der Compiler wendet eine kleine Strukturoptimierung an, die Strukturen zulässt, die kleiner sind als 8 Bytes (oder größer, wenn alle Werte Gleit Komma sind), die in Registern zurückgegeben werden sollen. Nur größere Strukturen werden herauf gestuft, um einen ausgeblendeten und vom Aufrufer zugewiesenen Rückgabewert zu verwenden.
* C++ behandelt diese als Element Funktionen. Der Compiler führt dies *immer* durch Einfügen eines ausgeblendeten Parameters (einen Zeiger auf einen vom Aufrufer zugeordneten Rückgabewert) als zweiten Parameter hinter dem- `this` Zeiger. Außerdem wird derselbe Zeiger zurückgegeben wie der Rückgabewert.

Dieser Schalter zwingt die c-Definition der Schnittstellen im resultierenden Header dazu, dass der Implementierer C++ verwendet hat, und dass der c-Code stattdessen explizit die C++ ABI verwenden sollte. Dies impliziert, dass die Funktion einen ausgeblendeten Parameter für den Rückgabewert Zeiger enthält und diesen Zeiger anstelle der Struktur direkt zurückgibt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>
