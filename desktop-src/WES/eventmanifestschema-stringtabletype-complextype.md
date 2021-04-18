---
title: Komplexer stringtabletype-Typ
description: Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können. | Komplexer stringtabletype-Typ
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Stringtabletype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365266"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="a3858-105">Komplexer stringtabletype-Typ</span><span class="sxs-lookup"><span data-stu-id="a3858-105">StringTableType Complex Type</span></span>

<span data-ttu-id="a3858-106">Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.</span><span class="sxs-lookup"><span data-stu-id="a3858-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a3858-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3858-107">Child elements</span></span>



| <span data-ttu-id="a3858-108">Element</span><span class="sxs-lookup"><span data-stu-id="a3858-108">Element</span></span>                                                              | <span data-ttu-id="a3858-109">type</span><span class="sxs-lookup"><span data-stu-id="a3858-109">Type</span></span> | <span data-ttu-id="a3858-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3858-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="a3858-111">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a3858-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="a3858-112">Definiert eine lokalisierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a3858-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a3858-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="a3858-113">Attributes</span></span>



| <span data-ttu-id="a3858-114">Name</span><span class="sxs-lookup"><span data-stu-id="a3858-114">Name</span></span>       | <span data-ttu-id="a3858-115">type</span><span class="sxs-lookup"><span data-stu-id="a3858-115">Type</span></span>   | <span data-ttu-id="a3858-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3858-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3858-117">id</span><span class="sxs-lookup"><span data-stu-id="a3858-117">id</span></span>         | <span data-ttu-id="a3858-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3858-118">string</span></span> | <span data-ttu-id="a3858-119">Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichen folgen Tabelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a3858-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="a3858-120">Beispiel: "Printer. Connection".</span><span class="sxs-lookup"><span data-stu-id="a3858-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="a3858-121">StringType</span><span class="sxs-lookup"><span data-stu-id="a3858-121">stringType</span></span> | <span data-ttu-id="a3858-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3858-122">string</span></span> | <span data-ttu-id="a3858-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3858-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="a3858-124">value</span><span class="sxs-lookup"><span data-stu-id="a3858-124">value</span></span>      | <span data-ttu-id="a3858-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3858-125">string</span></span> | <span data-ttu-id="a3858-126">Die lokalisierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a3858-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="a3858-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3858-127">Remarks</span></span>

<span data-ttu-id="a3858-128">Sie können auf die Zeichen Folgen eines beliebigen manifestressyps verweisen, der das Message-Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="a3858-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="a3858-129">Um auf eine Zeichenfolge mit dem StringType-Zeichensatz "String" und der ID "Printer. Connection" zu verweisen, verwenden Sie $ (String. Printer. Connection) als Wert für das Message-Attribut.</span><span class="sxs-lookup"><span data-stu-id="a3858-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3858-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3858-130">Requirements</span></span>



| <span data-ttu-id="a3858-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3858-131">Requirement</span></span> | <span data-ttu-id="a3858-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a3858-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3858-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3858-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a3858-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3858-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a3858-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3858-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a3858-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3858-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





