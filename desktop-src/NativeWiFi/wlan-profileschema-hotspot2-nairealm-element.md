---
description: Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Nairealm-Element (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527791"
---
# <a name="nairealm-hotspot2-element"></a><span data-ttu-id="be540-103">Nairealm-Element (Hotspot2)</span><span class="sxs-lookup"><span data-stu-id="be540-103">NAIRealm (Hotspot2) Element</span></span>

<span data-ttu-id="be540-104">Eine Liste von NAI-Bereichs Bezeichnern (Network Access Identifier).</span><span class="sxs-lookup"><span data-stu-id="be540-104">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="be540-105">Einträge in dieser Liste sind normalerweise in der Form `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="be540-105">Entries in this list are usually of the form `user@domain`.</span></span> <span data-ttu-id="be540-106">Die Liste der NAI-Bereiche ist die bevorzugte Methode, um die meisten nicht mobilen Operatoren wie MSOs, Wireline-Operatoren und öffentliche Veranstaltungsorte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="be540-106">The NAI Realm list is the preferred method to identify most non-mobile operators like MSOs, wireline operators, and public venues.</span></span>

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="be540-107">Das-Element wird durch das [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="be540-107">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="be540-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be540-108">Child elements</span></span>



| <span data-ttu-id="be540-109">Element</span><span class="sxs-lookup"><span data-stu-id="be540-109">Element</span></span> | <span data-ttu-id="be540-110">type</span><span class="sxs-lookup"><span data-stu-id="be540-110">Type</span></span> | <span data-ttu-id="be540-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be540-111">Description</span></span>                                                   |
|---------|------|---------------------------------------------------------------|
| <span data-ttu-id="be540-112">name</span><span class="sxs-lookup"><span data-stu-id="be540-112">name</span></span>    |      | <span data-ttu-id="be540-113">Ein einzelner Bereichs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="be540-113">A single realm identifier.</span></span> <span data-ttu-id="be540-114">Normalerweise das Formular `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="be540-114">Usually of the form `user@domain`.</span></span> |



 

 



