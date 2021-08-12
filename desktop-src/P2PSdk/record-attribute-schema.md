---
description: Datensätze können anwendungsspezifische Attribute aufweisen, bei denen es sich um eine Sequenz von Name- oder Wertpaaren handelt, die als XML-Zeichenfolge im pszAttributes-Element der PEER \_ RECORD-Struktur dargestellt werden.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Datensatzattributschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597369d7214b51b94a74b777315bb2ce2beb280232be5fb29571376ad3fc93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612311"
---
# <a name="record-attribute-schema"></a>Datensatzattributschema

Datensätze können anwendungsspezifische Attribute aufweisen, bei denen es sich um eine Sequenz von Name- oder Wertpaaren handelt, die als XML-Zeichenfolge im **pszAttributes-Element** der [**PEER \_ RECORD-Struktur dargestellt**](/windows/desktop/api/P2P/ns-p2p-peer_record) werden. Die Attribute werden verwendet, um eine Datensatzsuche zu filtern, die durch Aufrufe von [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)initiiert wird. Dabei wird ein XML-Suchfilter verwendet, der [im](record-search-query-format.md) Abfrageformat für die Datensatzsuche als Parameter angegeben ist.

Ein Datensatzattribut kann einer der folgenden drei Typen sein:

-   **int** ist ein ganzzahliger Wert.
-   **date** ist ein datetime-Wert, der als eines der unter beschriebenen Standardformate dargestellt [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) wird.
-   **string** ist ein Unicode-Zeichenfolgenwert.

In der folgenden Liste sind die spezifischen Attributnamen aufgeführt, die von der Peerinfrastruktur reserviert werden:

-   **peerlastmodifiedby**
-   **peercrekollegd**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Beispiel für das Definieren von Datensatzattributen

Im folgenden Schemabeispiel wird veranschaulicht, wie Datensatzattribute definiert werden:

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
> Attributnamen müssen Sequenzen alphanumerischer Zeichen sein. Sonderzeichen wie Bindestriche ("-") und Unterstriche (" \_ ") sind in einem Attributnamen nicht zulässig.

 

Das folgende Beispiel für eine XML-Attributsequenz enthält die benutzerdefinierten **Attribute AuthenticationType** und **AuthExpires,** die im **pszAttributes-Element** von [**PEER RECORD angezeigt \_ werden.**](/windows/desktop/api/P2P/ns-p2p-peer_record)

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



