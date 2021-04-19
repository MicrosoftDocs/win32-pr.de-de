---
description: Eine Liste von PLMN-IDs (Public Land Mobile Network).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Network3GPP (Hotspot2)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355558"
---
# <a name="network3gpp-hotspot2-element"></a><span data-ttu-id="00f93-103">Network3GPP (Hotspot2)-Element</span><span class="sxs-lookup"><span data-stu-id="00f93-103">Network3GPP (Hotspot2) Element</span></span>

<span data-ttu-id="00f93-104">Eine Liste von PLMN-IDs (Public Land Mobile Network).</span><span class="sxs-lookup"><span data-stu-id="00f93-104">A list of Public Land Mobile Network (PLMN) IDs.</span></span>

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="00f93-105">Das-Element wird durch das [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="00f93-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="00f93-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00f93-106">Child elements</span></span>



| <span data-ttu-id="00f93-107">Element</span><span class="sxs-lookup"><span data-stu-id="00f93-107">Element</span></span> | <span data-ttu-id="00f93-108">type</span><span class="sxs-lookup"><span data-stu-id="00f93-108">Type</span></span> | <span data-ttu-id="00f93-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00f93-109">Description</span></span>                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f93-110">Plmnid</span><span class="sxs-lookup"><span data-stu-id="00f93-110">PLMNID</span></span>  |      | <span data-ttu-id="00f93-111">Eine einzelne PLMN-ID.</span><span class="sxs-lookup"><span data-stu-id="00f93-111">An individual PLMN ID.</span></span> <span data-ttu-id="00f93-112">Dies ist eine 5-oder 6-stellige Dezimalzahl, die dem MCC/MNC eines 3GPP-Netzwerks entspricht.</span><span class="sxs-lookup"><span data-stu-id="00f93-112">This is a 5 or 6 digit decimal number corresponding to the MCC/MNC of a 3GPP network.</span></span><br/> |



 

 




