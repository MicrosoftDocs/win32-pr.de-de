---
title: Benutzer-Marshalling
description: Benutzer-Marshalling im Remoteprozeduraufruf (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dcc9574b49a46b6e867fc4bca314944589ccf68b9d6e3fb8695a099eb255c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010847"
---
# <a name="user-marshal"></a>Benutzer-Marshalling

Das Benutzer-Marshalling verfügt über eine Formatzeichenfolge, die der Übertragung \_ ähnelt:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Die Flags<1> Byte bestehen aus dem oberen Flag nibble und dem unteren Ausrichtungsnabzeichen.

Die oberen 2 Bits des Flag-Nibbles werden verwendet, um zu beschreiben, ob der Wire-Typ als eindeutiger Zeiger, Verweiszeiger oder kein Zeiger definiert ist (es kann kein Ptr sein). Die folgenden Manifeste wurden definiert, um die Flags festzulegen/abzurufen:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

Der Ausrichtungsnuss des Flagworts behält die Kabelausrichtung des übertragenen Typs bei.

Der \_ Vierfachindex<2> ist ein Index der Vierfachzahl der Rückrufroutine der Marshallingfunktionen des Benutzers. Die Routinepositionen sind wie folgt: Dimensionierung, Marshalling, Unmarshaling und Freisetzungsroutine.

Die \_ Arbeitsspeichergröße des Benutzertyps \_ \_<2> bietet eine Größe für den benutzerspezifischen Typ, einschließlich unbekannter Typen.

Die Puffergröße des übertragenen \_ Typs \_<\_ 2> ist entweder 0 (null), wenn die Größe variiert, oder die tatsächliche feste Größe. Dies ist eine Optimierung, mit der MIDL Rückrufe beim Dimensionieren des Puffers und beim Freigeben überspringen kann.

## <a name="range"></a>Range

Die \[ \] Bereichsüberprüfung bietet zusätzliche Mittel für die Argumentvalidierung auf der NDR-Ebene. Der \[ \] Bereichsdeskriptor hat das folgende Format:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Die Flags nehmen den oberen Nibble und geben den unteren Nibble des zweiten Byte ein. Die niedrigen und hohen Werte hängen vom Typ der zu überprüfenden Variablen ab.

Die Flags sind als Erweiterungs fahrzeug vorgesehen. der Compiler hat den Nibble auf 0 (null) festgelegt.

 

 




