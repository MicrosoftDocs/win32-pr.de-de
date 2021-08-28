---
description: Ein Aufruf der PeerGroupSearchRecords-Funktion erfordert einen XML-Abfragezeichenfolgenparameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu bestimmen.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Abfrageformat der Datensatzsuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a130d937177d4f903bfe52b121b2d67f8720d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887002"
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

### <a name="elements-to-use-for-a-record-search"></a>Elemente, die für eine Datensatzsuche verwendet werden sollen

Das primäre Element in einer Datensatzsuche ist **peersearch,** das den Uniform Resource Identifier (URI) des zugeordneten Schemas im **xmlns-Attribut** enthält. Wenn **peersearch** als untergeordnetes Element verwendet wird, können Sie **und**, **die -Klausel** und **oder** als untergeordnete Elemente verwenden.

-   **und** : Das -Element **und** das -Element führt einen logischen AND-Vorgang für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **tags und** und **oder** können untergeordnete Elemente sein, und rekursive Ergebnisse ihrer untergeordneten Klauseln werden in den Vorgang eingeschlossen.

    Wenn Sie beispielsweise einen Datensatz abrufen möchten, der einen Namen wie James Peters und ein letztes Update enthält, das größer als 28.02.2003 ist, oder ein Erstellungsdatum, das kleiner als 31.01.2003 ist, verwenden Sie die folgende XML-Abfragezeichenfolge:

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

-   **clause:** Das **-Klauselelement** gibt eine grundlegende vergleichsregel an, die den Wert eines bestimmten Datensatzattributs mit dem Wert vergleicht, der zwischen dem öffnenden und dem schließenden Tag enthalten ist. Die **Typ-** und **Vergleichsattribute** müssen angegeben **werden, um** den durchzuführenden Vergleichsvorgang anzugeben. Beispielsweise wird eine einfache Suche, die angibt, dass alle übereinstimmenden Datensätze einen **peererstellten** Wert aufweisen müssen, der james Peters entspricht, in der XML-Abfragezeichenfolge wie folgt angezeigt:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Zu den allgemeinen **Typattributen** gehören **int,** **string** und **date**. Das  Datumsattribut kann eines der unter beschriebenen Standarddatumsformate [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) sein.

    Die Werte für das **compare-Attribut** sind **gleich**, **notequal**, **less**, **greater**, **lessorequal** und **greaterorequal**.

<!-- -->

-   **oder** : Das -Element **oder** das -Element führt einen logischen OR-Vorgang für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **elemente oder** und **und** können untergeordnete Elemente sein, und rekursive Ergebnisse der untergeordneten Klauseln werden in den Vorgang eingeschlossen. Wenn Sie beispielsweise einen Datensatz abrufen möchten, der einen Namen wie James Peters oder ein letztes Update zwischen dem 31.01.2003 und dem 28.02.2003 enthält, verwenden Sie die folgende XML-Abfragezeichenfolge:

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

## <a name="more-information-about-a-record-search"></a>Weitere Informationen zur Datensatzsuche

Die erste Knotenebene nach **Peersearch** kann nur über ein Element verfügen. Nachfolgende untergeordnete Elemente dieses Elements können jedoch über viele Elemente auf derselben Ebene verfügen.

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

Die Abfrage schlägt fehl, da zwei Werte für die Übereinstimmung zurückgegeben werden, ohne in einen true/false-Wert aufgelöst zu werden. Das bedeutet, dass eine Klausel eine Abfrage für den Namen eines Datensatzes ist, der James Peters entspricht, und der AND-Vorgang mit den beiden Komponentenklauseln übereinstimmt. Das Ergebnis sind zwei logische TRUE/FALSE-Werte, die ungärr sind.

Um alle Datensätze abzurufen, die einen Namen wie James Peters und ein letztes Update zwischen dem 31.01.2003 und dem 28.02.2003 enthalten, platzieren Sie die **-Klausel** und die Tags **und** auf derselben Ebene zwischen öffnenden und schließenden **Tags.** Das folgende Beispiel zeigt die erfolgreiche Abfrage:

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

In der folgenden Liste sind weitere spezifische Informationen aufgeführt, die Sie kennen müssen, um eine erfolgreiche Abfrage schreiben zu können:

-   Die Tags **und** und **oder** können nicht zwischen öffnenden und schließenden **Klauseltags** gefunden werden, da sie in dieser Konfiguration als Teil des Werts interpretiert werden, mit dem eine Übereinstimmung gefunden werden soll. Dies führt zu einem Fehler oder einer fehlgeschlagenen Übereinstimmung.
-   Jedes Paar von **- und** **- oder** öffnenden und schließenden Tags muss mindestens einen untergeordneten Knoten enthalten.
-   Ein Satz von Elementen mit 0 (null) ist in diesem Schema nicht zulässig.

## <a name="record-attributes"></a>Datensatzattribute

Mithilfe des [Datensatzattributschemas](record-attribute-schema.md)kann ein Benutzer Datensatzattribute erstellen, die das **ATTRIB-XML-Attribut** in einem Klauselelement angibt. Attribute für einen neuen Datensatz werden hinzugefügt, indem das **pszAttributes-Element** von [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) auf eine XML-Zeichenfolge mit dem im Schema angegebenen Format festgelegt wird.

Die Peerinfrastruktur reserviert die folgenden Attributnamen:

-   **peerlastmodifiedby**
-   **peercrestrichd**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen können verwendet werden, um übereinstimmende Muster auszudrücken oder andere Sonderzeichen mit Escapezeichen zu escapen. Diese Zeichen werden in der folgenden Tabelle beschrieben. 

| Zeichenmuster | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Das Platzhalterzeichen. Wenn dieses Zeichen in einem Klauselwert gefunden wird, entspricht es 0-n Zeichen eines beliebigen Werts, einschließlich Leerzeichen und nicht alphanumerischer Zeichen. Beispiel:<br/> " <clause attrib="peercreatorid" type="string" compare="equal"> James P \* &lt; /clause &gt; "<br/> Diese Klausel gleicht alle **peercredauerd-Werte** mit dem Vornamen "James" und einem Nachnamen ab "P" ab.<br/> |
| \\\*              | Ein Sternchen mit Escapezeichen. Diese Sequenz entspricht einem Sternchenzeichen.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Das Platzhalterzeichen mit einem Zeichen. Wenn dieses Zeichen in einem Klauselwert gefunden wird, entspricht es jedem einzelnen Zeichen, einschließlich Leerzeichen und nicht alphanumerischen Zeichen. Zum Beispiel:<br/> " <clause attrib="filename" type="string" compare="equal"> data-0?.xml&lt; /clause &gt; "<br/> Diese Klausel entspricht **Dateinamenwerten** wie "data-01.xml" und "data-0B.xml".<br/>                              |
| \\?               | Ein Fragezeichen mit Escapezeichen. Diese Sequenz entspricht einem Fragezeichen.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Ein umgekehrter Schrägstrich mit Escapestrich. Diese Sequenz entspricht einem einzelnen umgekehrten Schrägstrich.                                                                                                                                                                                                                                                                                                                                                               |



 

Wenn die Zeichensequenz ungültig ist, gibt die [**PeerGroupSearchRecords-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) den Fehler **E \_ INVALIDARG** zurück. Eine ungültige Sequenz ist jede Sequenz, die ein Zeichen vom Typ \\ "" (umgekehrter Schrägstrich) nicht unmittelbar gefolgt von einem \* ""-Zeichen (Sternchen) und einem "?" enthält. (Fragezeichen) oder ein anderes Zeichen vom Typ " \\ " (umgekehrter Schrägstrich).

 

 




