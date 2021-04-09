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
# <a name="record-search-query-format"></a><span data-ttu-id="30726-103">Suchabfrage Format aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="30726-103">Record Search Query Format</span></span>

<span data-ttu-id="30726-104">Ein Aufrufen der Funktion " [**Peer groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) " erfordert einen XML-Abfrage Zeichenfolgen-Parameter, der verwendet wird, um die grundlegenden Kriterien einer Suche zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="30726-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="30726-105">Verwenden Sie das folgende Schema, um eine XML-Zeichenfolge zu formulieren:</span><span class="sxs-lookup"><span data-stu-id="30726-105">Use the following schema to formulate an XML string:</span></span>

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

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="30726-106">Für eine Daten Satz Suche zu verwendende Elemente</span><span class="sxs-lookup"><span data-stu-id="30726-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="30726-107">Das primäre Element in einer Daten Satz Suche ist " **Peer Search**", das die Uniform Resource Identifier (URI) des zugeordneten Schemas im **xmlns** -Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="30726-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="30726-108">Wenn " **Peer Search** " als untergeordnetes Element verwendet wird, können Sie **und**,- **Klausel** und **oder** als untergeordnete Elemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="30726-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="30726-109">**und** -das- **und** -Element führt eine logische and-Operation für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="30726-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="30726-110">Andere **-** und- **oder** -Tags können untergeordnete Elemente sein, und rekursive Ergebnisse ihrer untergeordneten Klauseln sind im-Vorgang enthalten.</span><span class="sxs-lookup"><span data-stu-id="30726-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="30726-111">Wenn Sie z. b. einen Datensatz mit einem Namen, der mit James Peters identisch ist, und ein letztes Update, das größer als 2/28/2003 ist, oder ein Erstellungsdatum, das kleiner als 1/31/2003 ist, abrufen möchten, verwenden Sie die folgende XML-Abfrage Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="30726-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

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

-   <span data-ttu-id="30726-112">**Klausel** : das **Klauselelement gibt** eine grundlegende Vergleichs Regel an, die den Wert eines bestimmten Daten Satz Attributs mit dem Wert vergleicht, der zwischen den öffnenden und schließenden Tags enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="30726-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="30726-113">Der **Typ** und die **Vergleichs** Attribute müssen angegeben werden. **vergleichen** gibt den auszuführenden Vergleichs Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="30726-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="30726-114">Beispielsweise muss eine einfache Suche, die alle übereinstimmenden Datensätze anzeigt, einen Wert von " **Peer-kreatorid** " aufweisen, der "James Peters" entspricht, wie folgt in der XML-Abfrage Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="30726-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="30726-115">Allgemeine **Typattribute** sind **int**, **String** und **Date**.</span><span class="sxs-lookup"><span data-stu-id="30726-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="30726-116">Das **Date** -Attribut kann eines der Standard Datumsformate sein, das unter beschrieben wird [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="30726-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="30726-117">Werte für das **Compare** -Attribut sind **gleich**, **NotEqual**, **less**, **größer**, **lessOrEqual** und **greaterOrEqual**.</span><span class="sxs-lookup"><span data-stu-id="30726-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="30726-118">**oder** : das- **oder** -Element führt eine logische OR-Operation für eine oder mehrere Klauseln aus, die zwischen den öffnenden und schließenden Tags enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="30726-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="30726-119">Andere **-und-und** **-** Elemente können untergeordnete Elemente sein, und rekursive Ergebnisse der untergeordneten Klauseln sind im-Vorgang enthalten.</span><span class="sxs-lookup"><span data-stu-id="30726-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="30726-120">Wenn Sie z. b. einen Datensatz abrufen möchten, der einen Namen wie James Peters oder ein letztes Update zwischen 1/31/2003 und 2/28/2003 enthält, verwenden Sie die folgende XML-Abfrage Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="30726-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

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

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="30726-121">Weitere Informationen zu einer Daten Satz Suche</span><span class="sxs-lookup"><span data-stu-id="30726-121">More Information About a Record Search</span></span>

<span data-ttu-id="30726-122">Die erste Ebene der Knoten nach **peersearch** darf nur ein Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="30726-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="30726-123">Nachfolgende untergeordnete Elemente dieses Elements können jedoch viele Elemente auf derselben Ebene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="30726-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="30726-124">Die folgende Suchabfrage ist falsch:</span><span class="sxs-lookup"><span data-stu-id="30726-124">The following search query is incorrect:</span></span>

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

<span data-ttu-id="30726-125">Die Abfrage schlägt fehl, da zwei Werte für die Übereinstimmung zurückgegeben werden, ohne dass Sie in einen true/false-Wert aufgelöst werden. Dies bedeutet, dass eine Klausel eine Abfrage für den Namen eines Datensatzes ist, der auf James Peters festgelegt ist, und der-Vorgang und der-Vorgang mit den beiden</span><span class="sxs-lookup"><span data-stu-id="30726-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="30726-126">Das Ergebnis sind zwei logische true/false-Werte, die widersprüchlich sind.</span><span class="sxs-lookup"><span data-stu-id="30726-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="30726-127">Zum Abrufen aller Datensätze, die einen Namen wie James Peters und ein letztes Update zwischen 1/31/2003 und 2/28/2003 enthalten, platzieren Sie die- **Klausel** und die **-** Tags, die sich auf derselben Ebene befinden, zwischen öffnenden und schließenden **-und-** Tags.</span><span class="sxs-lookup"><span data-stu-id="30726-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="30726-128">Das folgende Beispiel zeigt die erfolgreiche Abfrage:</span><span class="sxs-lookup"><span data-stu-id="30726-128">The following example shows you the successful query:</span></span>

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

<span data-ttu-id="30726-129">Die folgende Liste enthält weitere Informationen, die Sie kennen müssen, um eine erfolgreiche Abfrage zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="30726-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="30726-130">Die Tags **and** und **or** können nicht zwischen öffnenden **und schließenden** klauseltags gefunden werden, da Sie in dieser Konfiguration als Teil des Werts interpretiert werden, mit dem abgeglichen wird, was zu einem Fehler oder einer fehlgeschlagenen Entsprechung führt.</span><span class="sxs-lookup"><span data-stu-id="30726-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="30726-131">Jedes Paar von **-** und- **oder** -öffnenden und schließenden Tags muss mindestens einen untergeordneten Knoten enthalten.</span><span class="sxs-lookup"><span data-stu-id="30726-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="30726-132">Ein Nullsatz von Elementen ist in diesem Schema nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="30726-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="30726-133">Attribute aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="30726-133">Record Attributes</span></span>

<span data-ttu-id="30726-134">Mithilfe des [Datensatz-Attribut Schemas](record-attribute-schema.md)kann ein Benutzerdaten Satz Attribute erstellen, die vom XML-Attribut **atelemb** in einem clause-Element angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="30726-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="30726-135">Attribute für einen neuen Datensatz werden hinzugefügt, indem der **pszattribute** -Member des [**Peer \_ Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record) mithilfe des im Schema angegebenen Formats auf eine XML-Zeichenfolge festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="30726-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="30726-136">Die Peer Infrastruktur reserviert die folgenden Attributnamen:</span><span class="sxs-lookup"><span data-stu-id="30726-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="30726-137">**"Peer Last ModifiedBy"**</span><span class="sxs-lookup"><span data-stu-id="30726-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="30726-138">**"Peer-kreatorid"**</span><span class="sxs-lookup"><span data-stu-id="30726-138">**peercreatorid**</span></span>
-   <span data-ttu-id="30726-139">**"Peer Last ModificationTime"**</span><span class="sxs-lookup"><span data-stu-id="30726-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="30726-140">**Peer RecordID**</span><span class="sxs-lookup"><span data-stu-id="30726-140">**peerrecordid**</span></span>
-   <span data-ttu-id="30726-141">**"Peer RecordType"**</span><span class="sxs-lookup"><span data-stu-id="30726-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="30726-142">**"Peer-erkreationtime"**</span><span class="sxs-lookup"><span data-stu-id="30726-142">**peercreationtime**</span></span>
-   <span data-ttu-id="30726-143">**"Peer Last ModificationTime"**</span><span class="sxs-lookup"><span data-stu-id="30726-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="30726-144">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="30726-144">Special Characters</span></span>

<span data-ttu-id="30726-145">Bestimmte Zeichen können zum Ausdrücken von übereinstimmenden Mustern oder zum Escapezeichen für andere Sonderzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30726-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="30726-146">Diese Zeichen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="30726-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="30726-147">Zeichen Muster</span><span class="sxs-lookup"><span data-stu-id="30726-147">Character pattern</span></span> | <span data-ttu-id="30726-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30726-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="30726-149">Das Platzhalter Zeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-149">The wildcard character.</span></span> <span data-ttu-id="30726-150">Wenn dieses Zeichen in einem-klauselwert vorkommt, entspricht es 0-n-Zeichen eines beliebigen Werts, einschließlich Leerzeichen und nicht alphanumerischen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="30726-151">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="30726-151">For example:</span></span><br/> <span data-ttu-id="30726-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="30726-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="30726-153">Diese Klausel entspricht allen Werten von " **Peer-up-** ID" mit dem Vornamen "James" und einem Nachnamen, der mit "P" beginnt.</span><span class="sxs-lookup"><span data-stu-id="30726-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="30726-154">Ein mit Escapezeichen versehen.</span><span class="sxs-lookup"><span data-stu-id="30726-154">An escaped asterisk.</span></span> <span data-ttu-id="30726-155">Diese Sequenz entspricht einem Sternchen-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="30726-156">?</span><span class="sxs-lookup"><span data-stu-id="30726-156">?</span></span>                 | <span data-ttu-id="30726-157">Das Platzhalter Zeichen mit einem einzelnen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-157">The single-character wildcard character.</span></span> <span data-ttu-id="30726-158">Wenn dieses Zeichen in einem-klauselwert vorkommt, entspricht es einem beliebigen einzelnen Zeichen, einschließlich Leerzeichen und nicht alphanumerischen Zeichen. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="30726-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="30726-159">"<clause attrib="filename" type="string" compare="equal">Data-0?. XML</clause>"</span><span class="sxs-lookup"><span data-stu-id="30726-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="30726-160">Diese Klausel entspricht **Dateinamen** Werten wie "data-01.xml" und "data-0B.xml".</span><span class="sxs-lookup"><span data-stu-id="30726-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="30726-161">\\?</span><span class="sxs-lookup"><span data-stu-id="30726-161">\\?</span></span>               | <span data-ttu-id="30726-162">Ein Fragezeichen mit Escapezeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-162">An escaped question mark.</span></span> <span data-ttu-id="30726-163">Diese Sequenz entspricht einem Fragezeichen.</span><span class="sxs-lookup"><span data-stu-id="30726-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="30726-164">Ein umgekehrter umgekehrter Schrägstrich.</span><span class="sxs-lookup"><span data-stu-id="30726-164">An escaped backslash.</span></span> <span data-ttu-id="30726-165">Diese Sequenz entspricht einem einzelnen umgekehrten Schrägstrich.</span><span class="sxs-lookup"><span data-stu-id="30726-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="30726-166">Wenn die Zeichenfolge ungültig ist, gibt die Funktion " [**Peer groupsearchrecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) " den Fehler **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="30726-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="30726-167">Eine ungültige Sequenz ist eine beliebige Sequenz, die einen " \\ " (umgekehrter Schrägstrich) enthält, auf den nicht unmittelbar ein " \* " (Sternchen), ein "?"-Zeichen folgt. (Fragezeichen) oder ein anderer " \\ "-Zeichen (umgekehrter Schrägstrich).</span><span class="sxs-lookup"><span data-stu-id="30726-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




