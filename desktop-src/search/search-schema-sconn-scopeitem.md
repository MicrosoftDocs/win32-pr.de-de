---
description: Das- <scopeItem> Element stellt einen einzelnen Eintrag in der Ausschluss-/Inklusions Bereichs Tabelle dar.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: scopeitem-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128492"
---
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="7761d-103">scopeitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="7761d-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="7761d-104">Das- <scopeItem> Element stellt einen einzelnen Eintrag in der Ausschluss-/Inklusions Bereichs Tabelle dar.</span><span class="sxs-lookup"><span data-stu-id="7761d-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="7761d-105"><scopeItem> erweitert den standardmäßigen shelllinktype-Typ durch Hinzufügen von drei neuen Elementen, die das einschließen und Ausschließen von Ordnern steuern, die Tiefe der Ergebnisse steuern und den Speicherort des Bereichs angeben.</span><span class="sxs-lookup"><span data-stu-id="7761d-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="7761d-106">Wenn das- <scope> Element vorhanden ist, ist dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7761d-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="7761d-107">Sie verfügt über drei untergeordnete Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7761d-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7761d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7761d-108">Syntax</span></span>


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



## <a name="element-information"></a><span data-ttu-id="7761d-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7761d-109">Element Information</span></span>



| <span data-ttu-id="7761d-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="7761d-110">Parent Element</span></span>                                                           | <span data-ttu-id="7761d-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7761d-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="7761d-112">Scope-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="7761d-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="7761d-113">[Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope-mode.md).</span><span class="sxs-lookup"><span data-stu-id="7761d-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="7761d-114">[Scope-Element (Suchconnector-Schema)](search-schema-sconn-scope-depth.md).</span><span class="sxs-lookup"><span data-stu-id="7761d-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="7761d-115">[scopeitem-URL-Element (Suchconnector-Schema)](search-schema-sconn-scope-url.md).</span><span class="sxs-lookup"><span data-stu-id="7761d-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7761d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7761d-116">Remarks</span></span>

<span data-ttu-id="7761d-117">Verwenden <scope> Sie das-Element und das- <scopeItem> Element, um zu ermitteln, welche Orte gesucht werden sollen und welche Standorte von der Suche ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="7761d-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="7761d-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7761d-118">Example</span></span>

<span data-ttu-id="7761d-119">Das folgende Beispiel zeigt einen Suchbereich, der c: \\ examplefolder und alle seine untergeordneten Ordner mit Ausnahme von c: \\ examplefolder \\ excludebug enthält.</span><span class="sxs-lookup"><span data-stu-id="7761d-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



