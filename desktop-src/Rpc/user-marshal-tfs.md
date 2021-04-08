---
title: Benutzer Mars Hallen
description: Benutzer Mars Hall im Remote Prozedur Aufruf (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856140"
---
# <a name="user-marshal"></a>Benutzer Mars Hallen

Der Benutzer Mars Hall hat eine Format Zeichenfolge, die der folgenden ähnelt \_ :

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Die Flags<1> Byte bestehen aus dem oberen Flag-Halbbyte und dem unteren Ausrichtungs-Halbbyte.

Die oberen 2 Bits des Flag-Halbbyte werden verwendet, um zu beschreiben, ob der Wire-Typ als eindeutiger Zeiger, Verweis Zeiger oder kein Zeiger definiert ist (er kann kein PTR sein). Die folgenden Manifeste wurden definiert, um die Flags festzulegen/zu erhalten:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

Der Ausrichtungs Halbbyte des flagworts behält die Netzwerk Ausrichtung des übertragenen Typs bei.

Der vierfache \_ Index<2> ist ein Index der Rückruf Routine, vervierfachen der Benutzer Mars Hall Funktionen. Die Routine Positionen lauten wie folgt: Größenanpassung, Marshalling, Marshalling und Freigeben von Routinen.

Die Arbeits \_ Speichergröße des Benutzer Typs \_ \_<2> bietet eine Größe für den benutzerspezifischen Typ, einschließlich unbekannter Typen.

Die übertragene \_ \_ typpuffer \_ Größe<2> ist entweder 0 (null), wenn die Größe variiert, oder die tatsächliche Größe. Dies ist eine Optimierung, die es mittlerer l ermöglicht, Rückrufe bei der Größenanpassung des Puffers und auch bei der Freigabe zu überspringen.

## <a name="range"></a>Range

Die \[ Bereichs \] Überprüfung bietet zusätzliche Mittel für die Argument Validierung auf der NDR-Ebene. Der \[ Bereichs \] Deskriptor weist das folgende Format auf:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Die Flags nehmen den oberen Halbbyte und den Typ den unteren Halbbyte des zweiten bytes. Der niedrige und hohe Wert hängen vom Typ der Variablen ab, die geprüft werden soll.

Die Flags sind als Erweiterungs Fahrzeuge gedacht. der Compiler hat das Halbbyte auf 0 (null) festgelegt.

 

 




