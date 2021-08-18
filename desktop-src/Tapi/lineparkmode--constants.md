---
description: Die \_ LINEPARKMODE-Bitflagkonstanten beschreiben verschiedene Arten von Parkaufrufen.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: LINEPARKMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3070ad3f9e56de5e4e1a026b5f779c59469e947ff55b530e9d5b414a1b3b53b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140003"
---
# <a name="lineparkmode_-constants"></a>\_LINEPARKMODE-Konstanten

Die **\_ LINEPARKMODE-Bitflagkonstanten** beschreiben verschiedene Arten von Parkaufrufen.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ DIRECTED**
</dt> <dd> <dl> <dt>



Gibt den gerichteten Aufrufpark an. Die Adresse, an der der Aufruf geparkt werden soll, muss für den Switch angegeben werden.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ NONDIRECTED**
</dt> <dd> <dl> <dt>



Gibt einen nicht gerichteten Aufrufpark an. Die Adresse, an der der Aufruf geparkt wird, wird vom Switch ausgewählt und vom Switch für die Anwendung bereitgestellt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die **\_ LINEPARKMODE-Konstanten** werden beim Parken eines Aufrufs verwendet. Sehen Sie sich die Adressgerätefunktionen einer Zeile an, um herauszufinden, welcher Parkmodus verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




