---
description: Ein Aufrufen der Funktion "Peer groupsearchrecords" erfordert einen XML-Abfrage Zeichenfolgen-Parameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu ermitteln.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Suchabfrage Format aufzeichnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867007"
---
# <a name="record-search-query-format"></a>Suchabfrage Format aufzeichnen

Ein Aufrufen der Funktion " [**Peer groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) " erfordert einen XML-Abfrage Zeichenfolgen-Parameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu ermitteln. Verwenden Sie das folgende Schema, um eine XML-Zeichenfolge zu formulieren:

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

### <a name="elements-to-use-for-a-record-search"></a>Für eine Daten Satz Suche zu verwendende Elemente

Das primäre Element in einer Daten Satz Suche ist " **Peer Search**", das die Uniform Resource Identifier (URI) des zugeordneten Schemas im **xmlns** -Attribut enthält. Wenn " **Peer Search** " als untergeordnetes Element verwendet wird, können Sie **und**,- **Klausel** und **oder** als untergeordnete Elemente verwenden.

-   **und** -das- **und** -Element führt eine logische and-Operation für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **-** und- **oder** -Tags können untergeordnete Elemente sein, und rekursive Ergebnisse ihrer untergeordneten Klauseln sind im-Vorgang enthalten.

    Wenn Sie z. b. einen Datensatz mit einem Namen, der mit James Peters identisch ist, und ein letztes Update, das größer als 2/28/2003 ist, oder ein Erstellungsdatum, das kleiner als 1/31/2003 ist, abrufen möchten, verwenden Sie die folgende XML-Abfrage Zeichenfolge:

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

-   **Klausel** : das **Klauselelement gibt** eine grundlegende Vergleichs Regel an, die den Wert eines bestimmten Daten Satz Attributs mit dem Wert vergleicht, der zwischen den öffnenden und schließenden Tags enthalten ist. Der **Typ** und die **Vergleichs** Attribute müssen angegeben werden. **vergleichen** gibt den auszuführenden Vergleichs Vorgang an. Beispielsweise muss eine einfache Suche, die alle übereinstimmenden Datensätze anzeigt, einen Wert von " **Peer-kreatorid** " aufweisen, der "James Peters" entspricht, wie folgt in der XML-Abfrage Zeichenfolge

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Allgemeine **Typattribute** sind **int**, **String** und **Date**. Das **Date** -Attribut kann eines der Standard Datumsformate sein, das unter beschrieben wird [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Werte für das **Compare** -Attribut sind **gleich**, **NotEqual**, **less**, **größer**, **lessOrEqual** und **greaterOrEqual**.

<!-- -->

-   **oder** : das- **oder** -Element führt eine logische OR-Operation für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind. Andere **-und-und** **-** Elemente können untergeordnete Elemente sein, und rekursive Ergebnisse der untergeordneten Klauseln sind im-Vorgang enthalten. Wenn Sie z. b. einen Datensatz abrufen möchten, der einen Namen wie James Peters oder ein letztes Update zwischen 1/31/2003 und 2/28/2003 enthält, verwenden Sie die folgende XML-Abfrage Zeichenfolge:

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

## <a name="more-information-about-a-record-search"></a>Weitere Informationen zu einer Daten Satz Suche

Die erste Ebene der Knoten nach **peersearch** darf nur ein Element aufweisen. Nachfolgende untergeordnete Elemente dieses Elements können jedoch viele Elemente auf derselben Ebene aufweisen.

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

Die Abfrage schlägt fehl, da zwei Werte für die Übereinstimmung zurückgegeben werden, ohne dass Sie in einen true/false-Wert aufgelöst werden. Dies bedeutet, dass eine Klausel eine Abfrage für den Namen eines Datensatzes ist, der auf James Peters festgelegt ist, und der-Vorgang und der-Vorgang mit den beiden Das Ergebnis sind zwei logische true/false-Werte, die widersprüchlich sind.

Zum Abrufen aller Datensätze, die einen Namen wie James Peters und ein letztes Update zwischen 1/31/2003 und 2/28/2003 enthalten, platzieren Sie die- **Klausel** und die **-** Tags, die sich auf derselben Ebene befinden, zwischen öffnenden und schließenden **-und-** Tags. Das folgende Beispiel zeigt die erfolgreiche Abfrage:

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

Die folgende Liste enthält weitere Informationen, die Sie kennen müssen, um eine erfolgreiche Abfrage zu schreiben:

-   Die Tags **and** und **or** können nicht zwischen öffnenden **und schließenden** klauseltags gefunden werden, da Sie in dieser Konfiguration als Teil des Werts interpretiert werden, mit dem abgeglichen wird, was zu einem Fehler oder einer fehlgeschlagenen Entsprechung führt.
-   Jedes Paar von **-** und- **oder** -öffnenden und schließenden Tags muss mindestens einen untergeordneten Knoten enthalten.
-   Ein Nullsatz von Elementen ist in diesem Schema nicht zulässig.

## <a name="record-attributes"></a>Attribute aufzeichnen

Mithilfe des [Datensatz-Attribut Schemas](record-attribute-schema.md)kann ein Benutzerdaten Satz Attribute erstellen, die vom XML-Attribut **atelemb** in einem clause-Element angegeben werden. Attribute für einen neuen Datensatz werden hinzugefügt, indem der **pszattribute** -Member des [**Peer \_ Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record) mithilfe des im Schema angegebenen Formats auf eine XML-Zeichenfolge festgelegt wird.

Die Peer Infrastruktur reserviert die folgenden Attributnamen:

-   **"Peer Last ModifiedBy"**
-   **"Peer-kreatorid"**
-   **"Peer Last ModificationTime"**
-   **Peer RecordID**
-   **"Peer RecordType"**
-   **"Peer-erkreationtime"**
-   **"Peer Last ModificationTime"**

## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen können zum Ausdrücken von übereinstimmenden Mustern oder zum Escapezeichen für andere Sonderzeichen verwendet werden. Diese Zeichen werden in der folgenden Tabelle beschrieben. 

| Zeichen Muster | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Das Platzhalter Zeichen. Wenn dieses Zeichen in einem-klauselwert vorkommt, entspricht es 0-n-Zeichen eines beliebigen Werts, einschließlich Leerzeichen und nicht alphanumerischen Zeichen. Beispiel:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"<br/> Diese Klausel entspricht allen Werten von " **Peer-up-** ID" mit dem Vornamen "James" und einem Nachnamen, der mit "P" beginnt.<br/> |
| \\\*              | Ein mit Escapezeichen versehen. Diese Sequenz entspricht einem Sternchen-Zeichen.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Das Platzhalter Zeichen mit einem einzelnen Zeichen. Wenn dieses Zeichen in einem-klauselwert vorkommt, entspricht es einem beliebigen einzelnen Zeichen, einschließlich Leerzeichen und nicht alphanumerischen Zeichen. Zum Beispiel:<br/> "<clause attrib="filename" type="string" compare="equal">Data-0?. XML</clause>"<br/> Diese Klausel entspricht **Dateinamen** Werten wie "data-01.xml" und "data-0B.xml".<br/>                              |
| \\?               | Ein Fragezeichen mit Escapezeichen. Diese Sequenz entspricht einem Fragezeichen.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Ein umgekehrter umgekehrter Schrägstrich. Diese Sequenz entspricht einem einzelnen umgekehrten Schrägstrich.                                                                                                                                                                                                                                                                                                                                                               |



 

Wenn die Zeichenfolge ungültig ist, gibt die Funktion " [**Peer groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) " den Fehler **E \_ invalidArg** zurück. Eine ungültige Sequenz ist eine beliebige Sequenz, die einen " \\ " (umgekehrter Schrägstrich) enthält, auf den nicht unmittelbar ein " \* " (Sternchen), ein "?"-Zeichen folgt. (Fragezeichen) oder ein anderer " \\ "-Zeichen (umgekehrter Schrägstrich).

 

 




