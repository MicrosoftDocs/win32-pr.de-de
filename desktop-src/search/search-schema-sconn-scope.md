---
description: Das optionale <scope> -Element gibt eine Auflistung von- <scopeItem> Elementen an, die die Inklusions-und Ausschlüsse für diesen bestimmten Suchconnector definieren.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Scope-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343651"
---
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="bf1c3-103">Scope-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="bf1c3-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="bf1c3-104">Das optionale <scope> -Element gibt eine Auflistung von- <scopeItem> Elementen an, die die Inklusions-und Ausschlüsse für diesen bestimmten Suchconnector definieren.</span><span class="sxs-lookup"><span data-stu-id="bf1c3-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="bf1c3-105">Wenn <scope> vorhanden ist, muss Sie mindestens ein Element enthalten <scopeItem> .</span><span class="sxs-lookup"><span data-stu-id="bf1c3-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="bf1c3-106">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="bf1c3-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1c3-107">Syntax</span></span>


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="bf1c3-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bf1c3-108">Element Information</span></span>



| <span data-ttu-id="bf1c3-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bf1c3-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="bf1c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf1c3-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="bf1c3-111">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="bf1c3-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="bf1c3-112">[scopeitem-Element (Suchconnector-Schema)](search-schema-sconn-scopeitem.md).</span><span class="sxs-lookup"><span data-stu-id="bf1c3-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf1c3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf1c3-113">Remarks</span></span>

<span data-ttu-id="bf1c3-114">Verwenden <scope> Sie das-Element und das- <scopeItem> Element, um zu ermitteln, welche Orte gesucht werden sollen und welche Standorte von der Suche ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="bf1c3-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="bf1c3-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bf1c3-115">Example</span></span>

<span data-ttu-id="bf1c3-116">Das folgende Beispiel zeigt einen Suchbereich, der c: \\ examplefolder und alle seine untergeordneten Ordner mit Ausnahme von c: \\ examplefolder \\ excludebug enthält.</span><span class="sxs-lookup"><span data-stu-id="bf1c3-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



