---
title: Connection (Connections)-Element
description: Definiert jede Konfigurationseinstellung und verknüpft Sie mit einem Namen. Das Connection-Element ist optional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Verbindungselement EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340594"
---
# <a name="connection-connections-element"></a><span data-ttu-id="4305f-105">Connection (Connections)-Element</span><span class="sxs-lookup"><span data-stu-id="4305f-105">Connection (Connections) Element</span></span>

<span data-ttu-id="4305f-106">Das **Connection (Connections)** -Element definiert jede Konfigurationseinstellung und ordnet ihr einen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="4305f-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="4305f-107">Das **Connection** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4305f-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4305f-108">Das **Connection** -Element wird durch das [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4305f-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4305f-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4305f-109">Child elements</span></span>



| <span data-ttu-id="4305f-110">Element</span><span class="sxs-lookup"><span data-stu-id="4305f-110">Element</span></span>                                                                 | <span data-ttu-id="4305f-111">type</span><span class="sxs-lookup"><span data-stu-id="4305f-111">Type</span></span>   | <span data-ttu-id="4305f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4305f-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4305f-113">**EAP**</span><span class="sxs-lookup"><span data-stu-id="4305f-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="4305f-114">Identifiziert das EAP-Konfigurationselement.</span><span class="sxs-lookup"><span data-stu-id="4305f-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="4305f-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="4305f-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="4305f-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4305f-116">string</span></span> | <span data-ttu-id="4305f-117">Hiermit wird der Name der zu definierenden Verbindung erfasst und die Identifizierung mehrerer Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4305f-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="4305f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4305f-118">Requirements</span></span>



| <span data-ttu-id="4305f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4305f-119">Requirement</span></span> | <span data-ttu-id="4305f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4305f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4305f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4305f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4305f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4305f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4305f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4305f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4305f-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4305f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4305f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4305f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4305f-126">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4305f-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4305f-127">**Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="4305f-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="4305f-128">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4305f-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4305f-129">**Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="4305f-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="4305f-130">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="4305f-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4305f-131">eapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="4305f-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





