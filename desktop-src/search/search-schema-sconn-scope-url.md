---
description: Das- <url> Element gibt eine URL an, die den Gültigkeitsbereich des Suchconnector darstellt. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: scopeitem-URL-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862143"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="c5f3f-104">scopeitem-URL-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="c5f3f-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="c5f3f-105">Das- <url> Element gibt eine URL an, die den Gültigkeitsbereich des Suchconnector darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="c5f3f-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f3f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f3f-107">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="c5f3f-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c5f3f-108">Element Information</span></span>



| <span data-ttu-id="c5f3f-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c5f3f-109">Parent Element</span></span>                                                                   | <span data-ttu-id="c5f3f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5f3f-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c5f3f-111">scopeitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="c5f3f-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c5f3f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5f3f-112">Remarks</span></span>

<span data-ttu-id="c5f3f-113">Der Wert kann ein Pfad des lokalen Dateisystems oder eine URL sein.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="c5f3f-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5f3f-114">Example</span></span>

<span data-ttu-id="c5f3f-115">Das folgende Beispiel zeigt einen Suchbereich, der c: \\ examplefolder und alle seine untergeordneten Ordner mit Ausnahme von c: \\ examplefolder \\ excludebug enthält.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



