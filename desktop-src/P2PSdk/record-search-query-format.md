---
description: Ein Aufruf der PeerGroupSearchRecords-Funktion erfordert einen XML-Abfragezeichenfolgenparameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu bestimmen.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Abfrageformat der Datensatzsuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23457cfde6955927b3efdcce5ae2dff94480c7cf56849b418547fe2503a36830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517960"
---
# <a name="record-search-query-format"></a>Abfrageformat der Datensatzsuche

Ein Aufruf der [**PeerGroupSearchRecords-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) erfordert einen XML-Abfragezeichenfolgenparameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu bestimmen. Verwenden Sie das folgende Schema, um eine XML-Zeichenfolge zu formulieren:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a>Elemente, die für eine Datensatzsuche verwendet werden

Das primäre Element in einer Datensatzsuche ist **peersearch,** das die Uniform Resource Identifier (URI) des zugeordneten Schemas im **xmlns-Attribut** enthält. Wenn **peersearch** als untergeordnetes Element verwendet wird, können Sie **und**, die **-Klausel** und **oder** als untergeordnete Elemente verwenden.

-   **und** : Das **-Element und** das -Element führt einen logischen AND-Vorgang für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **-** und **- und -** oder -Tags können untergeordnete -Tags sein, und rekursive Ergebnisse ihrer untergeordneten Klauseln werden in den Vorgang eingeschlossen.

    Wenn Sie beispielsweise einen Datensatz abrufen möchten, der einen Namen enthält, der James Peters entspricht, und ein letztes Update, das größer als 28.02.2003 ist, oder ein Erstellungsdatum, das kleiner als 31.1.2003 ist, verwenden Sie die folgende XML-Abfragezeichenfolge:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   **clause:** Das **Klauselelement** gibt eine grundlegende Vergleichsregel an, die den Wert eines bestimmten Datensatzattributs mit dem Wert vergleicht, der zwischen dem öffnenden und dem schließenden Tag enthalten ist. Die **Typ-** und **Vergleichsattribute** müssen angegeben werden. **Compare** gibt den durchzuführenden Vergleichsvorgang an. Beispielsweise wird eine einfache Suche, die angibt, dass alle übereinstimmenden Datensätze einen **peercreierten Wert** haben müssen, der James Peters entspricht, in der XML-Abfragezeichenfolge wie folgt angezeigt:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Allgemeine **Typattribute** sind **int,** **string** und **date.** Das **Date-Attribut** kann eines der unter beschriebenen Standarddatumsformate [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) sein.

    Werte für das **compare-Attribut** **sind gleich**, **notequal**, **less**, **greater**, **lessorequal** und **greaterorequal**.

<!-- -->

-   **oder** : Das **- oder -Element** führt einen logischen OR-Vorgang für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **-** oder **- und -** und -Elemente können untergeordnete Elemente sein, und rekursive Ergebnisse der untergeordneten Klauseln werden in den Vorgang eingeschlossen. Wenn Sie beispielsweise einen Datensatz abrufen möchten, der einen Namen enthält, der James Peters entspricht, oder ein letztes Update zwischen dem 31.01.2003 und dem 28.02.2003, verwenden Sie die folgende XML-Abfragezeichenfolge:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a>Weitere Informationen zu einer Datensatzsuche

Die erste Knotenebene nach **peersearch** kann nur ein Element enthalten. Nachfolgende elemente dieses Elements können jedoch viele Elemente auf der gleichen Ebene haben.

Die folgende Suchabfrage ist falsch:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

Die Abfrage schlägt fehl, da zwei Werte für die Übereinstimmung zurückgegeben werden, ohne in einen true/false-Wert aufgelöst zu werden. Dies bedeutet, dass eine Klausel eine Abfrage für den Namen eines Datensatzes ist, der James Peters entspricht, und der AND-Vorgang mit den beiden Komponentenklauseln abgleicht. Das Ergebnis sind zwei logische TRUE-/FALSE-Werte, die unertreffend sind.

Um alle Datensätze zu erhalten, die einen Namen enthalten, der James Peters entspricht, und ein letztes Update zwischen dem 31.1.2003 und dem 28.02.2003, platzieren Sie die -Klausel und die -Tags auf der gleichen Ebene zwischen öffnenden und schließenden Tags und Tags.    Das folgende Beispiel zeigt die erfolgreiche Abfrage:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

In der folgenden Liste sind weitere spezifische Informationen aufgeführt, die Sie kennen müssen, um eine erfolgreiche Abfrage zu schreiben:

-   Die Tags **und** und **oder** können  nicht zwischen öffnenden und schließenden Klauseltags gefunden werden, da sie in dieser Konfiguration als Teil des Werts interpretiert werden, mit dem eine Übereinstimmung gefunden werden soll, was zu einem Fehler oder einer fehlgeschlagenen Übereinstimmung führt.
-   Jedes Paar von **und und** **oder öffnenden** und schließenden Tags muss mindestens einen oder mehrere untergeordnete Knoten enthalten.
-   Ein Satz von 0 (null) Elementen ist in diesem Schema nicht zulässig.

## <a name="record-attributes"></a>Datensatzattribute

Mithilfe des [Datensatzattributschemas](record-attribute-schema.md)kann ein Benutzer Datensatzattribute erstellen, die das **ATTRIB-XML-Attribut** in einem Klauselelement angibt. Attribute für einen neuen Datensatz werden hinzugefügt, indem das **pszAttributes-Element** von [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) mithilfe des im Schema angegebenen Formats auf eine XML-Zeichenfolge festgelegt wird.

Die Peerinfrastruktur reserviert die folgenden Attributnamen:

-   **peerlastmodifiedby**
-   **peercrekollegd**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen können verwendet werden, um übereinstimmende Muster auszudrücken oder andere Sonderzeichen mit Escapezeichen zu escapen. Diese Zeichen werden in der folgenden Tabelle beschrieben. 

| Zeichenmuster | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Das Platzhalterzeichen. Wenn dieses Zeichen in einem -Klauselwert gefunden wird, entspricht es 0-n Zeichen eines beliebigen Werts, einschließlich Leerzeichen und nicht alphanumerischer Zeichen. Beispiel:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James \* P</clause>"<br/> Diese Klausel gleicht alle **peercrewertierten Werte** mit dem Vornamen "James" und einem Nachnamen ab, der mit "P" beginnt.<br/> |
| \\\*              | Ein mit Escape versehenes Sternchen. Diese Sequenz entspricht einem Sternchenzeichen.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Das Platzhalterzeichen mit einem einzelnen Zeichen. Wenn dieses Zeichen in einem -Klauselwert gefunden wird, entspricht es jedem einzelnen Zeichen, einschließlich Leerzeichen und nicht alphanumerischen Zeichen. Zum Beispiel:<br/> "<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"<br/> Diese Klausel gleicht **Dateinamenwerte** wie "data-01.xml" und "data-0B.xml" ab.<br/>                              |
| \\?               | Ein Fragezeichen mit Escapezeichen. Diese Sequenz entspricht einem Fragezeichen.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Ein mit Escapestrichen bestrichener schräger Schrägstrich. Diese Sequenz entspricht einem einzelnen schrägen Schrägstrich.                                                                                                                                                                                                                                                                                                                                                               |



 

Wenn die Zeichenfolge ungültig ist, gibt die [**PeerGroupSearchRecords-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) den Fehler **E \_ INVALIDARG zurück.** Eine ungültige Sequenz ist eine Sequenz, die ein "" (schräger Schrägstrich) enthält, das nicht unmittelbar gefolgt von einem \\ " \* " (Sternchen)-Zeichen, einem "?" (Fragezeichen) oder ein anderes " \\ " (schräger Schrägstrich)

 

 




