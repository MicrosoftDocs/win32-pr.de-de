---
description: Datensätze können anwendungsspezifische Attribute aufweisen, bei denen es sich um eine Sequenz von Name-Wert-Paaren handelt, die im pszattribute-Member der Peer Daten Satzstruktur als XML-Zeichenfolge dargestellt werden \_ .
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Attribut Schema aufzeichnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353893"
---
# <a name="record-attribute-schema"></a>Attribut Schema aufzeichnen

Datensätze können anwendungsspezifische Attribute aufweisen, bei denen es sich um eine Sequenz von Name-Wert-Paaren handelt, die im **pszattribute** -Member der [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur als XML-Zeichenfolge dargestellt werden. Die Attribute werden verwendet, um eine Daten Satz Suche zu filtern, die durch Aufrufe von " [**Peer-groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)" initiiert wurde, die einen XML-Suchfilter verwendet, der im [Suchabfrage Format des Datensatzes](record-search-query-format.md) als Parameter angegeben

Ein Daten Satz Attribut kann einen der folgenden drei Typen aufweisen:

-   **int** ist ein ganzzahliger Wert.
-   **Date** ist ein DateTime-Wert, der als eines der Standardformate dargestellt wird, die unter beschrieben werden [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   die **Zeichen** Folge ist ein Unicode-Zeichen folgen Wert.

In der folgenden Liste sind die spezifischen Attributnamen aufgeführt, die von der Peer Infrastruktur reserviert werden:

-   **"Peer Last ModifiedBy"**
-   **"Peer-kreatorid"**
-   **"Peer Last ModificationTime"**
-   **Peer RecordID**
-   **"Peer RecordType"**
-   **"Peer-erkreationtime"**
-   **"Peer Last ModificationTime"**

## <a name="example-of-defining-record-attributes"></a>Beispiel für das Definieren von Daten Satz Attributen

Im folgenden Schema Beispiel wird gezeigt, wie Sie Daten Satz Attribute definieren:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> Attributnamen müssen Sequenzen von alphanumerischen Zeichen sein. Sonderzeichen wie Bindestriche ("-") und Unterstriche (" \_ ") sind in einem Attributnamen nicht zulässig.

 

Das folgende Beispiel für eine XML-Attribut Sequenz enthält die benutzerdefinierten **AuthenticationType** -und **authexpire** -Attribute, die im **pszattribute** -Member des [**Peer \_ Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record)angezeigt werden.

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



