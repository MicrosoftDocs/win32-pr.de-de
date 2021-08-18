---
title: RPC-Unions
description: Gekapselte und nicht gekapselte Unions und deren Format mit REMOTE PROCEDURE CALL (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5948a0557ea968a385324244d569d3578ec5d6c0dec4af5261866ed3ba2dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011018"
---
# <a name="rpc-unions"></a>RPC-Unions

Sowohl gekapselte als auch nicht gekapselte Unions verwenden eine gemeinsame \_ \_ Union-Arm-Auswahl<> Format:

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Die \_ Union-Arme<2> Feld bestehen aus zwei Teilen. Wenn es sich bei der Union um eine MIDL 1.0-Union handelt, enthalten die oberen 4 Bits die Ausrichtung des Union-Arms (Ausrichtung des größten ausgerichteten Arm). Andernfalls sind die oberen 4 Bits 0 (null). Die unteren 12 Bits enthalten die Anzahl der Arme in der Union. Anders gesagt:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

Die \_ \_ Offset-zu-Arm-Beschreibung \_<2> Felder enthalten einen relativen Offset mit Vorzeichen zur Typbeschreibung des Arms. Das Feld ist jedoch mit Optimierung für einfache Typen überladen. Für diese ist das obere Byte dieses Offsetfelds FC \_ MAGIC \_ UNION \_ BYTE (0x80), und das untere Byte des Shorts ist der tatsächliche Formatzeichentyp des Arms. Daher gibt es zwei Bereiche für die Offsetwerte: "80 *xx"* bedeutet, dass *xx* eine Typformatzeichenfolge ist. und alles andere innerhalb des Bereichs (80 FF . 7f FF) bedeutet einen tatsächlichen Offset. Dadurch werden Offsets vom Bereich <80 00 . 80 FF > nicht als Offsets verfügbar. Der Compiler überprüft dies ab MIDL-Version 5.1.164.

Die \_ \_ Standardarmbeschreibung<2> Feld gibt ggf. den Typ des Union-Arm für den Standardarm an. Wenn kein Standardarm für die Union angegeben ist, wird die \_ Standard-Armbeschreibung \_<2> Felds 0xFFFF, und eine Ausnahme wird ausgelöst, wenn der \_ Schalterwert nicht mit einem der Arm-Case-Werte übereinstimmt. Wenn der Standardarm angegeben, aber leer ist, ist die \_ Standard-Armbeschreibung \_<2> Feld 0 (null). Andernfalls hat die \_ Standard-Armbeschreibung \_<2> Feld die gleiche Semantik wie die \_ Offset-zu-Arm-Beschreibung \_<\_ 2> Feldern.

Es folgt eine Zusammenfassung:

-   0 – leerer Standardwert
-   FFFF – kein Standardwert
-   80xx : einfacher Typ
-   other – relativer Offset

## <a name="encapsulated-unions"></a>Gekapselte Unions

Eine gekapselte Union stammt aus einer speziellen Union-Syntax in IDL. Tatsächlich ist eine gekapselte Union eine Bündelstruktur mit einem diskriminanten Feld am Anfang der Struktur und der Union als einzigem anderen Member.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Der Switchtyp einer gekapselten Union \_<1> Feld hat zwei Teile. Der untere Nibble stellt den tatsächlichen Switchtyp bereit, und der obere Nibble stellt das Speicherinkrement bereit, das schrittweise überschritten werden soll. Dies ist eine Menge, die der Speicherzeiger erhöht werden muss, um über das Feld "switch is" hinauszuspringen. Dies \_ schließt alle Auffüllungen zwischen dem \_ Switchfeld is() der stub-konstruierten Struktur und dem tatsächlichen Union-Feld ein.

Die \_ Arbeitsspeichergröße<2> Feld entspricht nur der Größe der Union und ist mit nicht gekapselten Unions identisch. Um die Gesamtgröße der Struktur zu erhalten, die die Union enthält, fügen Sie die \_ Speichergröße<2> zur Schrittweisen Speicherinkrementierung hinzu, d. h. zum oberen Nibble des \_ Switchtyps<1> Feld, und richten Sie dann die Ausrichtung entsprechend der Inkrementierung aus.

## <a name="nonencapsulated-unions"></a>Nicht gekapselte Unions

Eine nicht gekapselte Union ist eine typische Situation, in der eine Union ein Argument oder Feld und der Schalter ein anderes Argument bzw. Feld ist.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Hierbei gilt:

Der \_ Schaltertyp<1> Feld ist ein Formatzeichen für den Diskriminanten.

Der Schalter \_ ist \_ deskriptor,<> Feld ein Korrelationsdeskriptor ist und je nachdem, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat. Für den Schalter ist jedoch \_ \_ description<>, wenn die Union in eine Struktur eingebettet ist, ist das Offsetfeld des Schalters \_ eine \_ Beschreibung,<> ist der Offset zum Schalter \_ feld von der Position der Union in der Struktur (nicht vom Anfang der Struktur).

Der Offset \_ zu \_ Größe und \_ \_ \_ Armbeschreibung<2> Felds gibt den Offset zur Größe der Union und der Armbeschreibung an, die mit der für gekapselte Unions identisch ist und von allen nicht gekapselten Unions des gleichen Typs gemeinsam genutzt wird:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 