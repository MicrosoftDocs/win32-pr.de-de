---
title: Ebene der Schema Unterstützung
description: In diesem Abschnitt werden die Details zur Ebene der Schema Unterstützung behandelt.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Schema Unterstützungs Ebene-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104554501"
---
# <a name="schema-support-level"></a>Ebene der Schema Unterstützung

In diesem Abschnitt werden die Details zur Ebene der Schema Unterstützung behandelt.


Das Schema unterstützt direkt Folgendes:

-   Sequenzen von Elementen.
-   Ableitung von Elementtypen.
-   Einfache Auswahl von Elementen (solche, die einer markierten Union zugeordnet sind).
-   Grundlegende Typen, die durch das XSD/.net-Binärformat definiert sind, einschließlich Bereiche (min/max).
-   Einfache Unterstützung für ein beliebiges Element (keine Einschränkungen für den Elementtyp).
-   Optionale Elemente und Attribute mit Standardwerten.
-   Wiederholen von Elementen mit Bereichen (min/max).
-   Nillable-Elemente.

Das Schema unterstützt Folgendes nicht direkt (was das "Fallback"-Verhalten impliziert):

-   Benutzerdefinierte Basis Typen.
-   Kompliziertere Auswahlmöglichkeiten.
-   Unbekannte Attribute werden abgelehnt.
-   Roundtrip für unbekannte Attribute.
-   Kompliziertere Unterstützung für jedes Element.
-   Das All-Konstrukt.
-   Key/keyref.

Im folgenden finden Sie eine ausführliche Aufschlüsselung der Unterstützung unterschiedlicher Schema Komponenten. Sie wird mit einem Datenvertrag in WCF verglichen, weil die Funktions Ähnlichkeit besteht. Der Unterschied wird beschrieben.

Im Allgemeinen gilt für Fall Back Verhalten:

-   Attribute werden auf die WS- \_ Zeichenfolge unterstützt.
-   der Inhalt des Elements wird auf den WS-XML-Puffer unterstützt \_ \_ .
-   complexType wird auf eine Struktur unterstützt, die ein Feld mit dem WS- \_ XML- \_ Puffer enthält.
-   Einfache Typen werden auf die WS- \_ Zeichenfolge unterstützt.

wsutil generiert Warnungen für Schema Komponenten, die derzeit nicht vollständig unterstützt werden. Die Anwendung muss möglicherweise eine zusätzliche Überprüfung durchführen, damit diese Komponenten benötigt werden. Die Überstunden "wsutil" kann verbessert werden, um einige der Funktionen zu verarbeiten, die derzeit in der Laufzeit unterstützt werden, z. b. Standardwert wsutil kann auch zusammen mit der Serialisierung verbessert werden, um andere Features wie Abstract zu unterstützen. Die Anzahl der nicht unterstützten Schema Komponenten kann im Laufe der Zeit reduziert werden.

## <a name="the-overall-schema-document"></a>Das Gesamt Schema Dokument

Eine globale Definition, die sich möglicherweise auf eingebettete Definitionen im Schema auswirkt. Dabei handelt es sich um globale Attribute, die auf alle Definitionen im Schema anwendbar sind.

<xs: Schema> Attribute

-   attributefromdefault wird ignoriert.
-   blockDefault wird ignoriert.
-   Element Form Default wird ignoriert. Dies unterscheidet sich von DataContract, da nicht qualifizierte Elemente in der Laufzeit unterstützt werden.
-   finalDefault wird ignoriert. Es gibt keine Unterstützung für die C-Sprache für das Konzept von "Final".
-   ID wurde ignoriert.
-   targetNamespace wird unterstützt und dem Dienst Namespace zugeordnet.
-   die Version wurde ignoriert.

<xs: Schema> Inhalt

-   Unterstützte einschließen; wsutil erfordert, dass alle erforderlichen Definitionen während der Kompilierungszeit als Eingabedateien verfügbar sind.
-   neu definieren wird ignoriert. Dies wird von wsutil nicht unterstützt.
-   Import wird unterstützt. wsutil erfordert, dass alle erforderlichen Definitionen während der Kompilierungszeit als Eingabedateien verfügbar sind.
-   simpleType unterstützt: siehe Abschnitt "einfacher Typ" weiter unten.
-   ComplexType unterstützt-siehe Abschnitt ' complexType '
-   die Gruppe wird ignoriert.
-   attributeGroup wird ignoriert.
-   unterstütztes Element; wird globalen Element Definitionen zugeordnet.
-   unterstützte Attribute wird globalen Attribut Definitionen zugeordnet.
-   Notation ignoriert

## <a name="complex-type"></a>Komplexer Typ

Ein komplexer Typ, der durch <xs: complexType-> dargestellt wird, kann eine Einschränkung des einfachen Typs oder komplexen Typs, der Erweiterung von einfachem Typ, Arrays oder Strukturen sein. Beachten Sie, dass in der Erweiterung von einfachen Typen keine Vererbung und keine xsi: Type-Unterstützung vorhanden ist.

<xs: complexType-> Attribute

-   Abstract generieren Sie eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   ID wurde ignoriert.
-   gemischt generiert eine Warnung über nicht unterstützte Funktion, Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer, wenn true.
-   der Name wird unterstützt und dem Strukturtyp Namen zugeordnet.

<xs: complexType> Inhalt

Dies ist eine Typdefinition für die-Struktur. die complexContent-Einschränkung wird nicht unterstützt.

-   complexContent unterstützt komplexe Inhalts Erweiterungen. Wird der Struktur Vererbung zugeordnet.
-   Gruppieren Sie derzeit ein Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer Feld. Kann gemäß dem untergeordneten Partikel unterstützt werden.
-   Auswahl wird als Union unterstützt. Dies wird im Datenvertrag nicht unterstützt.
-   Sequence supported-Zuordnungen zu Feldern einer Struktur
-   das Attribut wird mit einer Ausnahme von "verboten" unterstützt. Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer, wenn ' unzulässig ' ist.
-   attributeGroup unterstützt-Zuordnungs Sequenz von Attributen
-   anyAttribute wird ignoriert.
-   Attributegroupref unterstützt: entspricht der Sequenz von Attributen.
-   Groupref führt zurzeit ein Fall Back auf die Struktur mit dem WS \_ XML- \_ Puffer Feld aus Kann entsprechend der darunter liegenden Gruppe unterstützt werden.
-   Alle unterstützten, dem XML-Puffer Zuordnungen \_
-   (leer) unterstützte Zuordnung zu leerer Struktur Beschreibung ohne generierte Struktur.

<xs:sequence> in einem komplexen Typ: Inhalt

die Sequenz von minvorkommen = 1 und maxvorkommen = 1 wird von wsutil nur vollständig unterstützt. Andernfalls wird der komplexe Typ zurzeit auf den WS-XML-Puffer unterstützt \_ \_ . Sie kann als Array von Strukturen unterstützt werden.

-   unterstütztes Element; jede Instanz wird einem Feld in der Struktur zugeordnet.
-   Gruppen Fallback; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.
-   Alle Fallbacks; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.
-   Auswahl wird unterstützt. Ordnen Sie dem Union-Feld zu.
-   Sequenz Fall Back; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.
-   Alle unterstützten; dem XML- \_ Puffer zugeordnet.
-   (leer) unterstützt; ComplexType kann eine leere Struktur sein, wenn keine Attribute vorhanden sind.

## <a name="elements"></a>Elemente

<xs: Element>kann in drei Kontexten vorkommen.

-   Er kann in einem <xs: Sequence-> auftreten, der ein Feld einer regulären Struktur beschreibt. In diesem Fall muss das maxvorkommen-Attribut 1 sein. Das-Feld ist optional, wenn minvorkommen den Wert 0 hat.
-   Er kann in einem <xs: Sequence-> auftreten, der ein Feld eines Arrays beschreibt. In diesem Fall muss das maxvorkommen-Attribut größer als 1 oder unbegrenzt sein.
-   Sie kann in einem <xs: Schema-> als eine globale Element Beschreibung auftreten.

<xs: Element> in einer <xs: Sequence> oder <xs: Choice-> als Feld in einer Struktur

-   Verweis wird unterstützt. aufgelöst, um auf das globale Element zu verweisen.
-   Name unterstützt, wird dem Feldnamen zugeordnet.
-   der Typ wird unterstützt, der Feldtyp zugeordnet. Weitere Informationen finden Sie unter "Typzuordnung". Wenn nicht angegeben (und das Element keinen anonymen Typ enthält), wird xs: anyType angenommen.
-   Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   standardmäßige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   korrigiert: Warnung zu nicht unterstütztem Feature generieren, keine Änderung der Codegenerierung.
-   das Formular wird ignoriert. Unsere Serialisierungsebene unterstützt sowohl qualifizierte als auch nicht qualifizierte Formulare.
-   ID wurde ignoriert.
-   maxvorkommen ist einem einzelnen Datenfeld zugeordnet, wenn 1 entspricht. Sie wird einem Array Feld (sich wiederholendes Element) zugeordnet, wenn maxvorkommen größer als 1 ist.
-   minvorkommen wenn 0, werden die Feld Optionen auf Feld optional festgelegt \_ , wenn nillable nicht festgelegt ist.
-   nillable: das Feld ist nillable. Ausführlichere Informationen finden Sie unter [Serialisierung](serialization.md) .

<xs: Element> als globales Element: Attribute

die Attribute minvorkommen und maxvorkommen sind als globale Element Beschreibung ungültig. Die Anwendung kann die generierte Element Beschreibung in der Serialisierungsebene oder auf Kanal Ebenen direkt verwenden.

-   Abstract generieren Sie eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   standardmäßige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   korrigiert: Warnung zu nicht unterstütztem Feature generieren, keine Änderung der Codegenerierung.
-   ID wurde ignoriert.
-   Name unterstützt: Ordnen Sie den Namen der globalen Element Beschreibung zu und ist die Basis für den anonymen Typ, wenn angegeben.
-   nillable ignoriert: die Anwendung muss mit dem richtigen Flag aufgerufen werden.
-   substitutionGroup Fall Back auf Struktur mit WS- \_ XML- \_ Puffer, sofern festgelegt. "substitutionGroup" wird von wsutil nicht unterstützt.
-   der Typ wird unterstützt und dem Typ des Elements zugeordnet.

<xs: Element> als globales Element: Content

-   simpleType wird unterstützt. wird der Typdefinition zugeordnet.
-   complexType wird unterstützt. wird einem komplexen Typ zugeordnet.
-   eindeutige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung. "wsutil" unterstützt keine Element Einschränkungen.
-   Schlüssel generiert Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung. "wsutil" unterstützt keine Element Einschränkungen.
-   keyref generiert eine Warnung über eine nicht unterstützte Funktion, keine Änderung der Codegenerierung. "wsutil" unterstützt keine Element Einschränkungen.
-   Blitz Unterstützt ein Element ohne Typangabe wird als xs: anyType behandelt.

## <a name="simple-types"></a>Einfache Typen

<xs: simpleType-> Attribute

-   Abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   ID ignoriert
-   Name unterstützt, wird dem Typnamen zugeordnet.

<xs: simpleType-> Inhalt

-   Unterstützte Einschränkung, wird dem Enumerationstyp oder dem Bereich zugeordnet. Weitere Informationen finden Sie im Abschnitt "xs: simpleType-Einschränkungen".
-   Liste generiert Warnung zu nicht unterstützter Funktion, Fall Back auf XML- \_ Puffer.
-   Union generiert Warnung über nicht unterstützte Funktion, Fall Back auf XML- \_ Puffer.

## <a name="simple-type-restriction"></a>Einschränkung für einfache Typen

Bestimmte Facetten sind in ganzzahligen Typen und Zeichen folgen Typen zulässig, um Unterstützung für Bereiche und Enumerationen zuzulassen.

enumerationsunterstützung

<xs: Enumeration> einfache Typeinschränkung für den Basistyp der Zeichenfolge als Enumerationstyp behandelt. In diesem Fall muss das Basis Attribut vom Typ "String" sein. In Aufzählungs Fällen werden alle anderen Facetten ignoriert.

Bereich bei einfacher Typunterstützung

Einige Facetten sind Unterstützung für einfache Typen Unterstützung für den Typ. Die folgenden Einschränkungen gelten für ganzzahlige Typen und float/double-Typen. Einfache Typen mit anderen Facetten werden auf den WS- \_ Zeichen Folgentyp unterstützt.

-   minExclusive unterstützt
-   unterstützt minInclusive
-   maxExclusive unterstützt
-   unterstützt maxInclusive
-   totalDigits generiert eine Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   "fractionDigits" generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   Länge generiert Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   MinLength generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   MaxLength generiert eine Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   die Enumeration generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   Leerraum generiert Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.
-   Muster generieren Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.
-   Blitz Unterstützt.

MinLength und MaxLength in der Zeichenfolge werden zurzeit nicht unterstützt, ist aber ein wünschenswert, der unterstützt wird.

## <a name="inheritance"></a>Vererbung

Wsutil unterstützt die Vererbung komplexer Typen, d. h., eine Struktur kann von einer anderen Struktur erben, ähnlich der Schnittstellen Vererbung in C++. Dies erfolgt über <xs: complexcontentextension>. <xs: simplecontentextension> wird unterstützt, aber als einfache Struktur mit dem Basistyp als erstes Feld anstelle der Typvererbung generiert.

## <a name="typeprimitive-mapping"></a>Zuordnung von Typen zu primitivem Typen

Bezeichner müssen bei der Übersetzung von NCNames in XML normalisiert werden. Zeichen folgen sind nillable. Zeiger Typen sind nillable. ganzzahlige Typen und float/double sind nillable, und DefaultValue ist auf 0 festgelegt.

![Tabelle, die die Zuordnung zwischen XSD-Typen und sapplidatentypen anzeigt.](images/schematypemap.png)

 

 




