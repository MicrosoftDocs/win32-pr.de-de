---
description: Das- <templateInfo> Element ist ein Container für das foldertype-Element, das einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: templateingefo-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527305"
---
# <a name="templateinfo-element-library-schema"></a><span data-ttu-id="082c9-104">templateingefo-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="082c9-104">templateInfo Element (Library Schema)</span></span>

<span data-ttu-id="082c9-105">Das- <templateInfo> Element ist ein Container für das [foldertype](schema-library-foldertype.md) -Element, das einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt.</span><span class="sxs-lookup"><span data-stu-id="082c9-105">The <templateInfo> element is a container for the [folderType](schema-library-foldertype.md) element, which specifies a folder type for displaying the results from a query over this library.</span></span> <span data-ttu-id="082c9-106">Dieses Element ist optional und besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="082c9-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="082c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="082c9-107">Syntax</span></span>

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="082c9-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="082c9-108">Element Information</span></span>



| <span data-ttu-id="082c9-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="082c9-109">Parent Element</span></span>                                                               | <span data-ttu-id="082c9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="082c9-110">Child Elements</span></span>                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="082c9-111">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="082c9-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="082c9-112">foldertype-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="082c9-112">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)       |
|                                                                              | [<span data-ttu-id="082c9-113">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="082c9-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) |



 

## <a name="related-topics"></a><span data-ttu-id="082c9-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="082c9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="082c9-115">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="082c9-115">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="082c9-116">[Suchdienst-Beschreibungs Schema](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="082c9-116">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
