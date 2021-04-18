---
description: Dient zum Zuweisen von Enumerationstext zu diskreten Werten.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357780"
---
# <a name="enum"></a><span data-ttu-id="e5f97-103">enum</span><span class="sxs-lookup"><span data-stu-id="e5f97-103">enum</span></span>

<span data-ttu-id="e5f97-104">Dient zum Zuweisen von Enumerationstext zu diskreten Werten.</span><span class="sxs-lookup"><span data-stu-id="e5f97-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="e5f97-105">Eine beliebige Anzahl dieser Elemente kann unter einer [enumeratedlist](./propdesc-schema-enumeratedlist.md)vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e5f97-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="e5f97-106">Diese werden Programm gesteuert als ipropertyenumtype-Objekte dargestellt, deren [**ipropertyenumtype:: getenumtype**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) -Methode PET \_ diskretevalue zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e5f97-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f97-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5f97-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e5f97-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e5f97-108">Element Information</span></span>



| <span data-ttu-id="e5f97-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e5f97-109">Parent Element</span></span>                                         | <span data-ttu-id="e5f97-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5f97-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="e5f97-111">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="e5f97-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="e5f97-112">none</span><span class="sxs-lookup"><span data-stu-id="e5f97-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e5f97-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5f97-113">Attributes</span></span>



| <span data-ttu-id="e5f97-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="e5f97-114">Attribute</span></span> | <span data-ttu-id="e5f97-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5f97-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f97-116">value</span><span class="sxs-lookup"><span data-stu-id="e5f97-116">value</span></span>     | <span data-ttu-id="e5f97-117">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="e5f97-117">Public.</span></span> <span data-ttu-id="e5f97-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5f97-118">Required.</span></span> <span data-ttu-id="e5f97-119">Der diskrete Wert (Zeichenfolge oder Zahl), dem der Enumerationstext zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5f97-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="e5f97-120">text</span><span class="sxs-lookup"><span data-stu-id="e5f97-120">text</span></span>      | <span data-ttu-id="e5f97-121">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="e5f97-121">Public.</span></span> <span data-ttu-id="e5f97-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5f97-122">Required.</span></span> <span data-ttu-id="e5f97-123">Der Text, der verwendet wird, um den Enumerationswert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e5f97-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="e5f97-124">Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, damit Sie lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5f97-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="e5f97-125">Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="e5f97-125">mnemonics</span></span> | <span data-ttu-id="e5f97-126">**Windows 7 und höher.**</span><span class="sxs-lookup"><span data-stu-id="e5f97-126">**Windows 7 and later.**</span></span> <span data-ttu-id="e5f97-127">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="e5f97-127">Public.</span></span> <span data-ttu-id="e5f97-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5f97-128">Optional.</span></span> <span data-ttu-id="e5f97-129">Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e5f97-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="e5f97-130">Die Liste wird durch das \| Zeichen "" getrennt.</span><span class="sxs-lookup"><span data-stu-id="e5f97-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
