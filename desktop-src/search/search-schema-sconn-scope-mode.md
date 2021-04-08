---
description: Das- <mode> Element gibt an, ob die URL in den Gültigkeitsbereich des Suchconnector eingeschlossen oder ausgeschlossen werden soll. Die zulässigen Werte sind include und Exclude. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Mode-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750328"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="763b0-105">Mode-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="763b0-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="763b0-106">Das- <mode> Element gibt an, ob die URL in den Gültigkeitsbereich des Suchconnector eingeschlossen oder ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="763b0-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="763b0-107">Die zulässigen Werte sind `Include` und `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="763b0-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="763b0-108">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="763b0-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="763b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="763b0-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
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



## <a name="element-information"></a><span data-ttu-id="763b0-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="763b0-110">Element Information</span></span>



| <span data-ttu-id="763b0-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="763b0-111">Parent Element</span></span>                                                                   | <span data-ttu-id="763b0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="763b0-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="763b0-113">scopeitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="763b0-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="763b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="763b0-114">Remarks</span></span>

<span data-ttu-id="763b0-115">Ein ausgeschlossener Bereich kann nicht durchsucht oder durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="763b0-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="763b0-116">Sie können scopeitem-URLs Schachteln.</span><span class="sxs-lookup"><span data-stu-id="763b0-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="763b0-117">Beispielsweise können Sie einen übergeordneten Bereich und alle zugehörigen untergeordneten Elemente mit Ausnahme von einem übergeordneten Bereich einschließen, indem Sie die übergeordnete URL, den Tiefen Wert Deep und die untergeordnete URL hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="763b0-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="763b0-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="763b0-118">Example</span></span>

<span data-ttu-id="763b0-119">Das folgende Beispiel zeigt einen Suchbereich, der c: \\ examplefolder und alle seine untergeordneten Ordner mit Ausnahme von c: \\ examplefolder \\ excludebug enthält.</span><span class="sxs-lookup"><span data-stu-id="763b0-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



