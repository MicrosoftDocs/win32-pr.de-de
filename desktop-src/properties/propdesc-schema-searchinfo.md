---
description: Gibt an, wie die Windows-Such-Engine in Bezug auf eine angegebene Eigenschafts Definition konfiguriert wird.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: SearchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360177"
---
# <a name="searchinfo"></a><span data-ttu-id="a25e0-103">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="a25e0-103">searchInfo</span></span>

<span data-ttu-id="a25e0-104">Gibt an, wie die Windows-Such-Engine in Bezug auf eine angegebene Eigenschafts Definition konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="a25e0-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="a25e0-105">Wenn kein [SearchInfo]() -Element bereitgestellt wird, ist die Eigenschaft nicht in der Windows-Suchmaschine enthalten.</span><span class="sxs-lookup"><span data-stu-id="a25e0-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="a25e0-106">Dieses Element wurde für Windows 7 geändert.</span><span class="sxs-lookup"><span data-stu-id="a25e0-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="a25e0-107">Syntax für Windows 7</span><span class="sxs-lookup"><span data-stu-id="a25e0-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="a25e0-108">Syntax für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a25e0-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a25e0-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a25e0-109">Element Information</span></span>



| <span data-ttu-id="a25e0-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a25e0-110">Parent Element</span></span>                                                   | <span data-ttu-id="a25e0-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a25e0-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a25e0-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="a25e0-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="a25e0-113">Keine</span><span class="sxs-lookup"><span data-stu-id="a25e0-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="a25e0-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a25e0-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a25e0-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="a25e0-115">Attribute</span></span></th>
<th><span data-ttu-id="a25e0-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a25e0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a25e0-117">ininvertedindex</span><span class="sxs-lookup"><span data-stu-id="a25e0-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="a25e0-118">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-118">Public.</span></span> <span data-ttu-id="a25e0-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-119">Optional.</span></span> <span data-ttu-id="a25e0-120">Gibt an, ob der Eigenschafts Wert im invertierten Index gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a25e0-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="a25e0-121">Dadurch können Endbenutzer voll Text Abfragen für die Werte dieser Eigenschaft ausführen.</span><span class="sxs-lookup"><span data-stu-id="a25e0-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="a25e0-122">Die Standardeinstellung ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="a25e0-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a25e0-123">iscolumn</span><span class="sxs-lookup"><span data-stu-id="a25e0-123">isColumn</span></span></td>
<td><span data-ttu-id="a25e0-124">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-124">Public.</span></span> <span data-ttu-id="a25e0-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-125">Optional.</span></span> <span data-ttu-id="a25e0-126">Gibt an, ob die Eigenschaft auch in der Windows Search-Datenbank als Spalte gespeichert werden soll, damit unabhängige Softwareanbieter (ISVs) Prädikat basierte Abfragen erstellen können (z. b &quot; . Select \* Where &quot; System. Title &quot; = ' QQQ ' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="a25e0-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="a25e0-127">Wenn der Schema Ersteller es Endbenutzern (oder Entwicklern) ermöglichen möchte, Prädikat basierte Abfragen für die Eigenschaften zu erstellen, muss dieser Wert auf "true" festgelegt werden &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="a25e0-128">Die Standardeinstellung ist &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="a25e0-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a25e0-129">iscolumnsparse</span><span class="sxs-lookup"><span data-stu-id="a25e0-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="a25e0-130">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-130">Public.</span></span> <span data-ttu-id="a25e0-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-131">Optional.</span></span> <span data-ttu-id="a25e0-132">Der Standardwert ist &quot;true&quot;.</span><span class="sxs-lookup"><span data-stu-id="a25e0-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="a25e0-133">Wenn die Eigenschaft mehr wertig ist, ist dieses Attribut immer " &quot; true" &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a25e0-134">columnindextype</span><span class="sxs-lookup"><span data-stu-id="a25e0-134">columnIndexType</span></span></td>
<td><span data-ttu-id="a25e0-135">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-135">Public.</span></span> <span data-ttu-id="a25e0-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-136">Optional.</span></span> <span data-ttu-id="a25e0-137">Um das Sortieren und Gruppieren zu optimieren, kann das Windows Search-Modul sekundäre Indizes für Eigenschaften erstellen, deren iscolumn = &quot; true ist &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="a25e0-138">Dieses Attribut ist nur nützlich, wenn ininvertedindex &quot; &quot; in Windows Vista true ist oder wenn iscolumn &quot; in Windows 7 "true" ist &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="a25e0-139">Wenn die Eigenschaft tendenziell häufig von Benutzern sortiert wird, sollte dieses Attribut angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a25e0-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="a25e0-140">Der Standardwert in Windows Vista ist nicht &quot; indiziert &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="a25e0-141">Der Standardwert in Windows 7 ist &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="a25e0-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="a25e0-142">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="a25e0-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="a25e0-143"><strong>Notindiziert</strong>: erstellt nie einen Wertindex.</span><span class="sxs-lookup"><span data-stu-id="a25e0-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="a25e0-144"><strong>Ondisk</strong>: erstellt standardmäßig einen Wert Index für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a25e0-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="a25e0-145"><strong>Ondiskall</strong> (nur Windows 7 und höher): Erstellen Sie für diese Eigenschaft standardmäßig einen Wert Index, und wenn es sich um eine Vektor Eigenschaft handelt, ist dies auch ein Wert Index für alle verketteten Vektor Werte.</span><span class="sxs-lookup"><span data-stu-id="a25e0-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="a25e0-146"><strong>Ondiskvector</strong> (nur Windows 7 und höher): Erstellen Sie standardmäßig einen Wert Index für die verketteten Vektor Werte.</span><span class="sxs-lookup"><span data-stu-id="a25e0-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="a25e0-147"><strong>OnDemand</strong> (nur Windows 7 und höher): nur buildwertindizes nach Bedarf, d. h. nur das erste Mal, wenn Sie für eine Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a25e0-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a25e0-148">MaxSize</span><span class="sxs-lookup"><span data-stu-id="a25e0-148">maxSize</span></span></td>
<td><span data-ttu-id="a25e0-149">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-149">Public.</span></span> <span data-ttu-id="a25e0-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-150">Optional.</span></span> <span data-ttu-id="a25e0-151">Die maximale Größe (in Bytes), die für eine bestimmte Eigenschaft zulässig ist, die in der Windows Search-Datenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a25e0-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="a25e0-152">Der Standardwert lautet:</span><span class="sxs-lookup"><span data-stu-id="a25e0-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="a25e0-153"><strong>Windows Vista</strong>: 128 Bytes</span><span class="sxs-lookup"><span data-stu-id="a25e0-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="a25e0-154"><strong>Windows 7 und</strong>höher: 512 Bytes</span><span class="sxs-lookup"><span data-stu-id="a25e0-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="a25e0-155">Beachten Sie, dass diese maximale Größe in Bytes und nicht in Zeichen gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="a25e0-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="a25e0-156">Die maximale Anzahl von Zeichen hängt von ihrer Codierung ab.</span><span class="sxs-lookup"><span data-stu-id="a25e0-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a25e0-157">Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="a25e0-157">mnemonics</span></span></td>
<td><span data-ttu-id="a25e0-158"><strong>Windows 7 und höher.</strong></span><span class="sxs-lookup"><span data-stu-id="a25e0-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="a25e0-159">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="a25e0-159">Public.</span></span> <span data-ttu-id="a25e0-160">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a25e0-160">Optional.</span></span> <span data-ttu-id="a25e0-161">Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a25e0-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="a25e0-162">Die Liste wird durch das Zeichen "|" getrennt.</span><span class="sxs-lookup"><span data-stu-id="a25e0-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
