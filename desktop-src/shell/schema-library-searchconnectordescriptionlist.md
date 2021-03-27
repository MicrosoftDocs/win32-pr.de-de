---
description: Dieses <searchConnectorDescriptionList> Element enthält eine Liste von Suchconnectors, die in dieser Bibliothek enthaltene Standorte zugeordnet sind. Jeder Suchconnector wird durch ein- <searchConnectorDescription> Element definiert. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: searchconnectordescriptionlist-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980464"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="bee91-105">searchconnectordescriptionlist-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="bee91-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="bee91-106">Dieses <searchConnectorDescriptionList> Element enthält eine Liste von Suchconnectors, die in dieser Bibliothek enthaltene Standorte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bee91-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="bee91-107">Jeder Suchconnector wird durch ein- <searchConnectorDescription> Element definiert.</span><span class="sxs-lookup"><span data-stu-id="bee91-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="bee91-108">Dieses Element ist optional und besitzt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="bee91-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee91-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bee91-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="bee91-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="bee91-110">Element Information</span></span>



| <span data-ttu-id="bee91-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bee91-111">Parent Element</span></span>                                                               | <span data-ttu-id="bee91-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bee91-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee91-113">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="bee91-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="bee91-114">searchconnectordescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="bee91-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="bee91-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bee91-115">Remarks</span></span>

<span data-ttu-id="bee91-116">Suchconnectors für die Windows-Verbund Suche und die protokollhandlerbereiche können nicht in einer Bibliothek enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="bee91-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee91-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bee91-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee91-118">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="bee91-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="bee91-119">[Suchdienst-Beschreibungs Schema](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bee91-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
