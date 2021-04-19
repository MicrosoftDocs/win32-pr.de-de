---
title: Komplexer localizationtype-Typ
description: Definiert eine Gruppe lokalisierter Ressourcen, auf die im Manifest verwiesen wird. | Komplexer localizationtype-Typ
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- EventLog-Typ des komplexen lokalisierationstyp
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370370"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="c314c-105">Komplexer localizationtype-Typ</span><span class="sxs-lookup"><span data-stu-id="c314c-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="c314c-106">Definiert eine Gruppe lokalisierter Ressourcen, auf die im Manifest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c314c-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c314c-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c314c-107">Child elements</span></span>



| <span data-ttu-id="c314c-108">Element</span><span class="sxs-lookup"><span data-stu-id="c314c-108">Element</span></span>                                                                         | <span data-ttu-id="c314c-109">type</span><span class="sxs-lookup"><span data-stu-id="c314c-109">Type</span></span>                                                                       | <span data-ttu-id="c314c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c314c-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c314c-111">**verfügt**</span><span class="sxs-lookup"><span data-stu-id="c314c-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="c314c-112">Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c314c-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="c314c-113">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="c314c-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="c314c-114">**Stringtabletype**</span><span class="sxs-lookup"><span data-stu-id="c314c-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="c314c-115">Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.</span><span class="sxs-lookup"><span data-stu-id="c314c-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="c314c-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="c314c-116">Attributes</span></span>



| <span data-ttu-id="c314c-117">Name</span><span class="sxs-lookup"><span data-stu-id="c314c-117">Name</span></span>            | <span data-ttu-id="c314c-118">type</span><span class="sxs-lookup"><span data-stu-id="c314c-118">Type</span></span>   | <span data-ttu-id="c314c-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c314c-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c314c-120">culture</span><span class="sxs-lookup"><span data-stu-id="c314c-120">culture</span></span>         | <span data-ttu-id="c314c-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c314c-121">string</span></span> | <span data-ttu-id="c314c-122">Ein Sprachen Name, der die Kultur der lokalisierten Zeichen folgen in der Zeichen folgen Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="c314c-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="c314c-123">Beispiel: "en-US" für Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="c314c-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="c314c-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="c314c-124">fallbackCulture</span></span> | <span data-ttu-id="c314c-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c314c-125">string</span></span> | <span data-ttu-id="c314c-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c314c-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="c314c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c314c-127">Requirements</span></span>



| <span data-ttu-id="c314c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c314c-128">Requirement</span></span> | <span data-ttu-id="c314c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c314c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c314c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c314c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c314c-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c314c-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c314c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c314c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c314c-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c314c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





