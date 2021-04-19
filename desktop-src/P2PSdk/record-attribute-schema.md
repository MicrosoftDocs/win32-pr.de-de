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
# <a name="record-attribute-schema"></a><span data-ttu-id="0485a-103">Attribut Schema aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="0485a-103">Record Attribute Schema</span></span>

<span data-ttu-id="0485a-104">Datensätze können anwendungsspezifische Attribute aufweisen, bei denen es sich um eine Sequenz von Name-Wert-Paaren handelt, die im **pszattribute** -Member der [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Struktur als XML-Zeichenfolge dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0485a-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="0485a-105">Die Attribute werden verwendet, um eine Daten Satz Suche zu filtern, die durch Aufrufe von " [**Peer-groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)" initiiert wurde, die einen XML-Suchfilter verwendet, der im [Suchabfrage Format des Datensatzes](record-search-query-format.md) als Parameter angegeben</span><span class="sxs-lookup"><span data-stu-id="0485a-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="0485a-106">Ein Daten Satz Attribut kann einen der folgenden drei Typen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0485a-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="0485a-107">**int** ist ein ganzzahliger Wert.</span><span class="sxs-lookup"><span data-stu-id="0485a-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="0485a-108">**Date** ist ein DateTime-Wert, der als eines der Standardformate dargestellt wird, die unter beschrieben werden [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="0485a-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="0485a-109">die **Zeichen** Folge ist ein Unicode-Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="0485a-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="0485a-110">In der folgenden Liste sind die spezifischen Attributnamen aufgeführt, die von der Peer Infrastruktur reserviert werden:</span><span class="sxs-lookup"><span data-stu-id="0485a-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="0485a-111">**"Peer Last ModifiedBy"**</span><span class="sxs-lookup"><span data-stu-id="0485a-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="0485a-112">**"Peer-kreatorid"**</span><span class="sxs-lookup"><span data-stu-id="0485a-112">**peercreatorid**</span></span>
-   <span data-ttu-id="0485a-113">**"Peer Last ModificationTime"**</span><span class="sxs-lookup"><span data-stu-id="0485a-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="0485a-114">**Peer RecordID**</span><span class="sxs-lookup"><span data-stu-id="0485a-114">**peerrecordid**</span></span>
-   <span data-ttu-id="0485a-115">**"Peer RecordType"**</span><span class="sxs-lookup"><span data-stu-id="0485a-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="0485a-116">**"Peer-erkreationtime"**</span><span class="sxs-lookup"><span data-stu-id="0485a-116">**peercreationtime**</span></span>
-   <span data-ttu-id="0485a-117">**"Peer Last ModificationTime"**</span><span class="sxs-lookup"><span data-stu-id="0485a-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="0485a-118">Beispiel für das Definieren von Daten Satz Attributen</span><span class="sxs-lookup"><span data-stu-id="0485a-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="0485a-119">Im folgenden Schema Beispiel wird gezeigt, wie Sie Daten Satz Attribute definieren:</span><span class="sxs-lookup"><span data-stu-id="0485a-119">The following schema example shows you how to define record attributes:</span></span>

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
> <span data-ttu-id="0485a-120">Attributnamen müssen Sequenzen von alphanumerischen Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="0485a-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="0485a-121">Sonderzeichen wie Bindestriche ("-") und Unterstriche (" \_ ") sind in einem Attributnamen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0485a-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="0485a-122">Das folgende Beispiel für eine XML-Attribut Sequenz enthält die benutzerdefinierten **AuthenticationType** -und **authexpire** -Attribute, die im **pszattribute** -Member des [**Peer \_ Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0485a-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



