---
title: Schemaunterstützungsebene
description: In diesem Abschnitt werden die Details zur Ebene der Schemaunterstützung behandelt.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Webdienste auf Schemaunterstützungsebene für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6cae112e074d50b90425c1d8952f3b6c06463378d73767346742193b406d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026282"
---
# <a name="schema-support-level"></a>Schemaunterstützungsebene

In diesem Abschnitt werden die Details zur Ebene der Schemaunterstützung behandelt.


Das Schema unterstützt Folgendes direkt:

-   Sequenzen von Elementen.
-   Ableitung von Elementtypen.
-   Einfache Auswahlmöglichkeiten von Elementen (elemente, die einer markierten Union zugeordnet sind).
-   Grundlegende Typen, die durch das XSD-/.NET-Binärformat definiert werden, einschließlich Bereichen (min/max).
-   Einfache Unterstützung für jedes Element (keine Einschränkungen für den Elementtyp).
-   Optionale Elemente und Attribute mit Standardwerten.
-   Wiederholen von Elementen mit Bereichen (min/max).
-   Nillable-Elemente.

Das Schema unterstützt Folgendes nicht direkt (was das Fallbackverhalten impliziert):

-   Benutzerdefinierte Basistypen.
-   Kompliziertere Optionen.
-   Ablehnen unbekannter Attribute.
-   Roundtrips für unbekannte Attribute.
-   Kompliziertere Unterstützung für jedes Element.
-   Das all-Konstrukt.
-   Key/keyref.

Im Folgenden finden Sie eine ausführliche Aufschlüsselung der Unterstützung verschiedener Schemakomponenten. Es wird mit dem Datenvertrag in WCF verglichen, da die Funktionalität ähnlich ist. Der Unterschied wird beschrieben.

Im Allgemeinen gilt für Fallbackverhalten:

-   -Attribute werden auf WS \_ STRING zurückverlegt.
-   -Elementinhalt wird auf WS \_ XML BUFFER zurückverlegt. \_
-   complexType wird auf eine Struktur mit einem Feld von WS \_ XML BUFFER zurückverlegt. \_
-   Einfache Typen werden auf WS \_ STRING zurückverlegt.

wsutil generiert Warnungen für Schemakomponenten, die derzeit nicht vollständig unterstützt werden. Die Anwendung muss möglicherweise eine zusätzliche Überprüfung für diese Komponenten durchführen. Overtime wsutil kann verbessert werden, um einige der Features zu verarbeiten, die derzeit zur Laufzeit unterstützt werden, z. B. die Unterstützung von Standardwerten. wsutil kann auch zusammen mit der Serialisierung verbessert werden, um andere Features wie abstract zu unterstützen. Die Anzahl der nicht unterstützten Schemakomponenten kann im Laufe der Zeit reduziert werden.

## <a name="the-overall-schema-document"></a>Das allgemeine Schemadokument

Globale Definition, die sich auf eingebettete Definitionen im Schema auswirken kann. Dies sind globale Attribute, die auf alle Definitionen im Schema anwendbar sind.

<xs:schema> Attribute

-   attributeFromDefault Ignored.
-   blockDefault Ignored.
-   elementFormDefault Ignored. Dies unterscheidet sich von dataContract, da nicht qualifizierte Elemente zur Laufzeit unterstützt werden.
-   finalDefault Ignored. Es gibt keine C-Sprachunterstützung für das Konzept von final.
-   id Ignoriert.
-   targetNamespace Wird unterstützt und dem Dienstnamespace zugeordnet.
-   Version ignoriert.

<xs:schema> Inhalte

-   include Unterstützt; wsutil erfordert, dass während der Kompilierung alle erforderlichen Definitionen als Eingabedateien verfügbar sind.
-   neu definieren Ignoriert. wsutil unterstützt dies nicht.
-   Import unterstützt; wsutil erfordert, dass während der Kompilierung alle erforderlichen Definitionen als Eingabedateien verfügbar sind.
-   simpleType Unterstützt: Siehe abschnitt "simple type" weiter unten.
-   complexType unterstützt – siehe Abschnitt "complexType".
-   gruppe Ignoriert.
-   attributeGroup Ignoriert.
-   Unterstütztes Element; wird globalen Elementdefinitionen zugeordnet.
-   unterstütztes Attribut; wird globalen Attributdefinitionen zugeordnet.
-   notation Ignored

## <a name="complex-type"></a>Komplexer Typ

Komplexer Typ, der durch <xs:complexType> dargestellt wird, kann eine Einschränkung des einfachen Typs oder komplexen Typs, der Erweiterung eines einfachen Typs, von Arrays oder einer Struktur sein. Es wurde festgestellt, dass in Erweiterungen einfacher Typen keine Vererbung und keine xsi:type-Unterstützung vorhanden ist.

<xs:complexType> Attribute

-   abstract Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   block Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   final Warnung zu nicht unterstützter Funktion generieren, keine Änderung an der Codegenerierung.
-   id Ignoriert.
-   Mixed Warnung zu nicht unterstützter Funktion generieren, Fallback zur Struktur mit WS \_ XML \_ BUFFER bei TRUE.
-   name Unterstützt und strukturtypname zugeordnet.

inhalt <xs:complexType>

Dies ist die Typdefinition für structure. die ComplexContent-Einschränkung wird nicht unterstützt.

-   complexContent Unterstützt komplexe Inhaltserweiterungen. Karten, um die Vererbung zu strukturen.
-   group Derzeit fallback to structure with WS XML BUFFER field (Derzeit Fallback zur Struktur mit dem \_ WS-XML-PUFFERfeld). \_ Kann entsprechend dem darunter liegenden Partikel unterstützt werden.
-   Die Auswahl wird als Union unterstützt. Dies wird im Datenvertrag nicht unterstützt.
-   Sequence Supported – Zuordnung zu Feldern einer Struktur
-   -Attribut, das mit einer Ausnahme von "prohibited" unterstützt wird. fallback to structure with WS \_ XML \_ BUFFER if 'prohibited'.
-   attributeGroup unterstützt – Zuordnung zur Sequenz von Attributen
-   anyAttribute Ignored
-   AttributeGroupRef unterstützt : Wird der Sequenz von Attributen zugeordnet.
-   GroupRef: Derzeit wird ein Fallback auf die Struktur mit dem WS \_ XML \_ BUFFER-Feld verwendet. Kann entsprechend der darunter liegenden Gruppe unterstützt werden.
-   Unterstützt, XML BUFFER zugeordnet \_
-   (blank) Unterstützte Zuordnung zu einer leeren Strukturbeschreibung ohne generierte Struktur.

<xs:sequence> in einem komplexen Typ: Inhalt

wsutil unterstützt nur die Sequenz von minOccurs = 1 und maxOccurs = 1 vollständig. andernfalls wird der komplexe Typ derzeit auf WS \_ XML BUFFER zurückverlegt. \_ Sie kann als Array von -Strukturen unterstützt werden.

-   Unterstütztes Element; jede Instanz wird einem Feld in der -Struktur zugeordnet.
-   Gruppenfallback; complexType ist ein Fallback auf WS \_ XML \_ BUFFER.
-   Alle Fallbacks; complexType ist ein Fallback auf WS \_ XML \_ BUFFER.
-   Unterstützte Auswahl; Dem Union-Feld zuordnen.
-   Sequenzfallback; complexType ist ein Fallback auf WS \_ XML \_ BUFFER.
-   unterstützt; zugeordnet zu XML \_ BUFFER.
-   (leer) unterstützt; complexType kann eine leere Struktur sein, wenn keine Attribute vorhanden sind.

## <a name="elements"></a>Elemente

<xs:element->kann in drei Kontexten auftreten.

-   Er kann innerhalb eines <xs:sequence-> auftreten, das ein Feld einer regulären Struktur beschreibt. In diesem Fall muss das maxOccurs-Attribut 1 sein. Das Feld ist optional, wenn minOccurs 0 ist.
-   Er kann innerhalb eines <xs:sequence-> auftreten, der ein Feld eines Arrays beschreibt. In diesem Fall muss das maxOccurs-Attribut größer als 1 oder "ungebunden" sein.
-   Er kann innerhalb eines <xs:schema-> als globale Elementbeschreibung auftreten.

<xs:element> innerhalb eines <xs:sequence-> oder <xs:choice-> als Feld in einer Struktur

-   ref unterstützt; aufgelöst, um auf das globale Element zu verweisen.
-   name Unterstützt, wird dem Feldnamen zugeordnet.
-   Der Typ Wird unterstützt, wird dem Feldtyp zugeordnet. Weitere Informationen finden Sie unter "Typzuordnung". Wenn keine Angabe erfolgt (und das Element keinen anonymen Typ enthält), wird xs:anyType angenommen.
-   block Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   Standard: Warnung zu nicht unterstützten Funktionen generieren, keine Änderung an der Codegenerierung.
-   Behoben: Warnung zu nicht unterstütztem Feature generieren, keine Änderung an der Codegenerierung.
-   Formular Ignoriert. Unsere Serialisierungsebene unterstützt sowohl qualifizierte als auch nicht qualifizierte Formulare.
-   id Ignoriert.
-   maxOccurs wird einem einzelnen Datenfeld zugeordnet, wenn gleich 1 ist. sie wird einem Arrayfeld (sich wiederholendes Element) zugeordnet, wenn maxOccurs größer als 1 ist.
-   minOccurs wenn 0, werden die Feldoptionen auf FIELD \_ OPTIONAL festgelegt, wenn nillable nicht festgelegt ist.
-   nillable Das Feld ist nillable. Weitere Informationen finden Sie unter [Serialisierung.](serialization.md)

<xs:element> als globales Element: Attribute

Die Attribute minOccurs und maxOccurs sind als globale Elementbeschreibung ungültig. Die Anwendung kann die generierte Elementbeschreibung direkt in der Serialisierungsschicht oder in Kanalebenen verwenden.

-   abstract Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   block Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   Standard: Warnung zu nicht unterstützten Funktionen generieren, keine Änderung an der Codegenerierung.
-   final Warnung zu nicht unterstützter Funktion generieren, keine Änderung an der Codegenerierung.
-   Behoben: Warnung zu nicht unterstütztem Feature generieren, keine Änderung an der Codegenerierung.
-   id Ignoriert.
-   name Supported: Ordnen Sie dem Namen der beschreibung des globalen Elements zu, und ist die Basis für den anonymen Typ, wenn angegeben.
-   nillable Ignored-application muss mit dem rechten Flag aufrufen.
-   ersatzGroup fallback to structure with WS XML BUFFER (Fallback zur Struktur mit WS \_ XML \_ BUFFER, falls festgelegt). wsutil unterstützt substitutionGroup nicht.
-   Geben Sie Unterstützt ein, und ordnen Sie dem Typ des Elements zu.

<xs:element> als globales Element: contents

-   simpleType unterstützt; wird der Typdefinition zugeordnet.
-   complexType unterstützt; wird einem komplexen Typ zugeordnet.
-   unique Warnung zu nicht unterstützter Funktion generieren, keine Änderung an der Codegenerierung. wsutil unterstützt keine Elementeinschränkungen.
-   Schlüssel Generiert eine Warnung zu nicht unterstützten Funktionen, keine Änderung an der Codegenerierung. wsutil unterstützt keine Elementeinschränkungen.
-   keyref Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung. wsutil unterstützt keine Elementeinschränkungen.
-   (leer) Unterstützt; -Element ohne Typspezifikation wird als xs:anyType behandelt.

## <a name="simple-types"></a>Einfache Typen

<xs:simpleType> Attribute

-   Letzte Warnung generieren zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   ID ignoriert
-   Name Unterstützt, wird dem Typnamen zugeordnet.

<xs:simpleType> Inhalte

-   Einschränkung unterstützt, wird dem Enumerationstyp oder -bereich zugeordnet. Weitere Informationen finden Sie im Abschnitt "xs:simpleType restrictions" (xs:simpleType-Einschränkungen).
-   Liste Warnung zu nicht unterstützter Funktion generieren, Fallback auf XML \_ BUFFER.
-   Union Generate warning about unsupported feature, fallback to XML \_ BUFFER.

## <a name="simple-type-restriction"></a>Einschränkung des einfachen Typs

Bestimmte Facets sind in ganzzahligen Typen und Zeichenfolgentypen zulässig, um Bereichs- und Enumerationsunterstützung zu ermöglichen.

Enumerationsunterstützung

<xs:enumeration> einfache Typeinschränkung für den Basistyp der Zeichenfolge wird als Enumerationstyp behandelt. In diesem Fall MUSS das Base-Attribut zeichenfolgentyp sein. Im Enumerationsfall werden alle anderen Facets ignoriert.

Bereich für Unterstützung für einfache Typen

Einige Facets werden in einfachen Typen unterstützt, die einen effektiven Bereich unterstützen, der für den Typ zulässig ist. Es folgen Einschränkungen für ganzzahlige Typen und float/double-Typen. Einfache Typen mit anderen Facets werden auf den WS STRING-Typ zurückverlegt. \_

-   minExclusive unterstützt
-   minInclusive unterstützt
-   maxExclusive unterstützt
-   maxInclusive unterstützt
-   totalDigits Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   fractionDigits Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   length Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   minLength Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   maxLength Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   enumeration Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   Leerraum Warnung zu nicht unterstütztem Feature generieren, keine Änderung an der Codegenerierung.
-   Muster Generiert eine Warnung zu nicht unterstützten Features, keine Änderung an der Codegenerierung.
-   (leer) Unterstützt.

minLength und maxLength für Zeichenfolgen werden derzeit nicht unterstützt, sind aber ein wünschenswertes Feature zur Unterstützung.

## <a name="inheritance"></a>Vererbung

Wsutil unterstützt die Vererbung komplexer Typen, d. h., eine Struktur kann von einer anderen Struktur erben, ähnlich der Schnittstellenvererbung in C++. Dies erfolgt über <xs:complexContentExtension>. <xs:simpleContentExtension-> wird unterstützt, wird jedoch als einfache Struktur mit Basistyp als erstes Feld anstelle von Typvererbung generiert.

## <a name="typeprimitive-mapping"></a>Zuordnung von Typen zu primitivem Typen

Bezeichner müssen normalisiert werden, wenn sie aus NCNames in XML übersetzt werden. Zeichenfolgen sind nillable; Zeigertypen sind nillable; ganzzahlige Typen und float/double sind nillable, und defaultValue ist auf 0 festgelegt.

![Tabelle mit der Zuordnung zwischen XSD-Typen und Sapphire-Datentypen.](images/schematypemap.png)

 

 




