---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: image-Element (Schema der Eigenschaftenbeschreibung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104988"
---
# <a name="image"></a><span data-ttu-id="d93db-103">image</span><span class="sxs-lookup"><span data-stu-id="d93db-103">image</span></span>

<span data-ttu-id="d93db-104">Es sollte nur ein [Bildelement für]() jedes übergeordnete Element geben.</span><span class="sxs-lookup"><span data-stu-id="d93db-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d93db-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d93db-106">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d93db-106">Element Information</span></span>



| <span data-ttu-id="d93db-107">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d93db-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="d93db-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d93db-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="d93db-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="d93db-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="d93db-110">Keine</span><span class="sxs-lookup"><span data-stu-id="d93db-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="d93db-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="d93db-111">Attributes</span></span>



| <span data-ttu-id="d93db-112">attribute</span><span class="sxs-lookup"><span data-stu-id="d93db-112">Attribute</span></span> | <span data-ttu-id="d93db-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d93db-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="d93db-114">res</span><span class="sxs-lookup"><span data-stu-id="d93db-114">res</span></span>       | <span data-ttu-id="d93db-115">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="d93db-115">Public.</span></span> <span data-ttu-id="d93db-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d93db-116">Required.</span></span> |



 

 

 
