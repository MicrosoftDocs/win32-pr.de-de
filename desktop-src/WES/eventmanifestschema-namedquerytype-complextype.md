---
title: Komplexer namedquerytype-Typ
description: Nicht verwendet. Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden. | Komplexer namedquerytype-Typ
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Namedquerytype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365043"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="05504-106">Komplexer namedquerytype-Typ</span><span class="sxs-lookup"><span data-stu-id="05504-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="05504-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="05504-107">Not used.</span></span> <span data-ttu-id="05504-108">Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden.</span><span class="sxs-lookup"><span data-stu-id="05504-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="05504-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05504-109">Child elements</span></span>



| <span data-ttu-id="05504-110">Element</span><span class="sxs-lookup"><span data-stu-id="05504-110">Element</span></span>                                                                       | <span data-ttu-id="05504-111">type</span><span class="sxs-lookup"><span data-stu-id="05504-111">Type</span></span>                                                                             | <span data-ttu-id="05504-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05504-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05504-113">**patternmaps**</span><span class="sxs-lookup"><span data-stu-id="05504-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="05504-114">**Patternmaplisttype**</span><span class="sxs-lookup"><span data-stu-id="05504-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="05504-115">Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05504-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="05504-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05504-116">Examples</span></span>

<span data-ttu-id="05504-117">Im folgenden Beispiel wird gezeigt, wie das [**namedqueries**](eventmanifestschema-namedqueries-metadatatype-element.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05504-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="05504-118">In diesem Beispiel wird der Inhalt der Meldungs Zeichenfolge in die Zeichenfolge eingefügt https://www .*Messagestring*. com.</span><span class="sxs-lookup"><span data-stu-id="05504-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="05504-119">Anschließend wird die Meldungs Zeichenfolge durch das Ergebnis ersetzt.</span><span class="sxs-lookup"><span data-stu-id="05504-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="05504-120">Wenn die Meldungs Zeichenfolge z. b. Microsoft enthält, würde die Abfrage die Microsoft-Nachrichten Zeichenfolge durch ersetzen https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="05504-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="05504-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05504-121">Requirements</span></span>



| <span data-ttu-id="05504-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05504-122">Requirement</span></span> | <span data-ttu-id="05504-123">Wert</span><span class="sxs-lookup"><span data-stu-id="05504-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05504-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05504-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05504-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05504-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05504-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05504-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05504-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05504-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





