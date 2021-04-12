---
title: RPC-Unions
description: Gekapselte und nicht gekapselte Unions und deren Format mit Remote Prozedur Aufruf (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473164"
---
# <a name="rpc-unions"></a>RPC-Unions

Sowohl gekapselte als auch nicht gekapselte Unions haben eine gemeinsame Union- \_ Arm- \_<> Auswahl

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Das \_ Feld Union Arms<2> besteht aus zwei Teilen. Wenn die Union eine Union im 1,0-Stil ist, enthalten die oberen 4 Bits die Ausrichtung des Union-Arm (Ausrichtung des größten ausgerichteten Arm). Andernfalls sind die oberen 4 Bits 0 (null). Die unteren 12 Bits enthalten die Anzahl der Waffen in der Union. Anders gesagt:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

Die Beschreibung des Offset- \_ zu- \_ Arm \_ -<2> Felder enthalten einen relativen Offset mit Vorzeichen zur Typbeschreibung des Arm-Typs. Allerdings wird das Feld mit Optimierung für einfache Typen überladen. Hierfür ist das obere Byte dieses Offset Felds FC \_ Magic \_ Union \_ Byte (0x80) und das untere Byte der Kurzform der tatsächliche Format Zeichentyp des Arm. Daher gibt es zwei Bereiche für die Offset Werte: "80 *xx*" bedeutet, dass *xx* eine typformatzeichenfolge ist. und alles andere innerhalb des Bereichs (80 ff. 7F) bedeutet einen tatsächlichen Offset. Dadurch werden Offsets aus dem Bereich <80 00. 80 FF > nicht als Offsets verfügbar. Der Compiler überprüft dies ab der 5.1.164 der mittleren Version.

Die Standard- \_ Arm- \_ Beschreibung<2> Feld gibt den Typ des Union-Arm-Werts für den Standardarm an (sofern vorhanden). Wenn kein Standardarm für die Union angegeben ist, wird die \_ Standardarm- \_ Beschreibung<2> Feld 0xFFFF verwendet, und es wird eine Ausnahme ausgelöst, wenn der Schalter Wert keinen der \_ Arm-Case-Werte entspricht. Wenn die Standardarm angegeben, aber leer ist, ist die standardmäßige \_ Arm- \_ Beschreibung<2> Feld NULL. Andernfalls weist die \_ \_ standardbeschreibungs-<2> Feld die gleiche Semantik wie die Offset- \_ zu- \_ Arm- \_ Beschreibung<2> Felder auf.

Im folgenden finden Sie eine Zusammenfassung:

-   0-leerer Standardwert
-   FFFF-kein Standardwert
-   80xx-einfacher Typ
-   anderer relativer Offset

## <a name="encapsulated-unions"></a>Gekapselt Unions

Eine gekapselte Union stammt aus einer speziellen Union-Syntax in IDL. Effektiv ist eine gekapselte Union eine Bündel Struktur mit einem Diskriminanten Feld am Anfang der Struktur und der Union als einziges anderes Element.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Der Switch-Typ einer gekapselten Union \_<1> Feld hat zwei Teile. Der untere Halbbyte bietet den eigentlichen Switchtyp, und der obere Halbbyte bietet das Arbeitsspeicher Inkrement für den Schritt, bei dem der Speicher Zeiger erhöht werden muss, um den Switch \_ is-Feld zu überspringen, der alle Auffüll Zeichen zwischen dem Switch \_ is ()-Feld der Stub-Struktur und dem eigentlichen Union-Feld einschließt.

Die Arbeitsspeicher \_ Größe<2> Feld entspricht nur der Größe der Union und ist mit nicht gekapselten Unions identisch. Wenn Sie die Gesamtgröße der Struktur abrufen möchten, die die Union enthält, fügen Sie die Arbeitsspeicher \_ Größe<2> zu Arbeitsspeicher Inkrement hinzu, um einen Prozedur Schritt auszuführen, d. h. den oberen Halbbyte des \_ Switchtyps<1> Feld, und richten Sie dann die Ausrichtung an, die dem Inkrement entspricht.

## <a name="nonencapsulated-unions"></a>Nicht gekapselt Unions

Eine nicht gekapselte Union ist eine typische Situation, in der eine Union ein Argument oder ein Feld ist und der Switch ein anderes Argument bzw. Feld ist.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Hierbei gilt:

Der \_ Switchtyp<1> Feld ist ein Formatzeichen für den Diskriminanten.

Der Schalter \_ ist \_ ein Deskriptor,<> Feld ein Korrelations Deskriptor ist und abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat. Für den Schalter ist jedoch \_ \_ Description<> wenn die Union in eine Struktur eingebettet ist, ist das Offset-Feld des Schalters \_ \_ Description<> der Offset zum Switch \_ ist das Feld von der Union-Position in der Struktur (nicht vom Anfang der Struktur).

Der Offset \_ - \_ zu \_ -Größe-und der \_ Arm \_ -Beschreibungs-<2> Feld gibt den Offset der Union-Größe und der Arm-Beschreibung an, die für gekapselte Unions identisch ist und von allen nicht gekapselten Unions desselben Typs gemeinsam genutzt wird:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 