---
description: Das <depth> -Element gibt an, ob der Bereich des Suchconnector untergeordnete URLs einschließen soll. Die zulässigen Werte sind tief und flach. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: tiefen Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958780"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="83021-105">tiefen Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="83021-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="83021-106">Das <depth> -Element gibt an, ob der Bereich des Suchconnector untergeordnete URLs einschließen soll.</span><span class="sxs-lookup"><span data-stu-id="83021-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="83021-107">Die zulässigen Werte sind `Deep` und `Shallow`.</span><span class="sxs-lookup"><span data-stu-id="83021-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="83021-108">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="83021-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="83021-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="83021-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="83021-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="83021-110">Element Information</span></span>



| <span data-ttu-id="83021-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="83021-111">Parent Element</span></span>                                                                   | <span data-ttu-id="83021-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83021-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="83021-113">scopeitem-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="83021-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="83021-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83021-114">Remarks</span></span>

<span data-ttu-id="83021-115">Wenn die Tiefe tiefer ist, können Benutzer Elemente in der URL-Ebene von scopeitem oder innerhalb von untergeordneten URLs durchsuchen oder durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="83021-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="83021-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="83021-116">Example</span></span>

<span data-ttu-id="83021-117">Das folgende Beispiel zeigt einen Suchbereich, der c: \\ FolderA und alle seine untergeordneten Ordner und c: \\ folderB, aber keinen seiner untergeordneten Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="83021-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



