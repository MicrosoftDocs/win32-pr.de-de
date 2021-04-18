---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Image-Element (Eigenschafts Beschreibungs Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358806"
---
# <a name="image"></a><span data-ttu-id="5f061-103">image</span><span class="sxs-lookup"><span data-stu-id="5f061-103">image</span></span>

<span data-ttu-id="5f061-104">Es darf nur ein [Bild]() Element für jedes übergeordnete Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5f061-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f061-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f061-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="5f061-106">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="5f061-106">Element Information</span></span>



| <span data-ttu-id="5f061-107">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f061-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="5f061-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f061-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="5f061-109">[](./propdesc-schema-enum.md) [Enumeration, enumbereich](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="5f061-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="5f061-110">Keine</span><span class="sxs-lookup"><span data-stu-id="5f061-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="5f061-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f061-111">Attributes</span></span>



| <span data-ttu-id="5f061-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="5f061-112">Attribute</span></span> | <span data-ttu-id="5f061-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f061-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="5f061-114">res</span><span class="sxs-lookup"><span data-stu-id="5f061-114">res</span></span>       | <span data-ttu-id="5f061-115">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="5f061-115">Public.</span></span> <span data-ttu-id="5f061-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f061-116">Required.</span></span> |



 

 

 
