---
title: Connections-Element
description: Erfahren Sie mehr über das Connections-Element. Dieses Element sammelt und enthält keine oder mehrere Verbindungselemente.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections-Element EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340534"
---
# <a name="connections-element"></a><span data-ttu-id="6d3ed-105">Connections-Element</span><span class="sxs-lookup"><span data-stu-id="6d3ed-105">Connections Element</span></span>

<span data-ttu-id="6d3ed-106">Das **Connections** -Element sammelt und enthält keine oder mehrere [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) -Elemente.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="6d3ed-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d3ed-107">Child elements</span></span>



| <span data-ttu-id="6d3ed-108">Element</span><span class="sxs-lookup"><span data-stu-id="6d3ed-108">Element</span></span>                                                                              | <span data-ttu-id="6d3ed-109">type</span><span class="sxs-lookup"><span data-stu-id="6d3ed-109">Type</span></span>   | <span data-ttu-id="6d3ed-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d3ed-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d3ed-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="6d3ed-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="6d3ed-112">Identifiziert das EAP-Konfigurationselement.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="6d3ed-113">**Verbindung**</span><span class="sxs-lookup"><span data-stu-id="6d3ed-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="6d3ed-114">Definiert jede Konfigurationseinstellung und verknüpft Sie mit einem Namen.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="6d3ed-115">Das [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="6d3ed-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="6d3ed-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="6d3ed-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6d3ed-117">string</span></span> | <span data-ttu-id="6d3ed-118">Hiermit wird der Name der zu definierenden Verbindung erfasst und die Identifizierung mehrerer Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="6d3ed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d3ed-119">Remarks</span></span>

<span data-ttu-id="6d3ed-120">Das **Connections** -Element wird nicht mit Legacy Methoden über die EAPHost-APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d3ed-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d3ed-121">Requirements</span></span>



| <span data-ttu-id="6d3ed-122">Role</span><span class="sxs-lookup"><span data-stu-id="6d3ed-122">Role</span></span> | <span data-ttu-id="6d3ed-123">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="6d3ed-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6d3ed-124">Client</span><span class="sxs-lookup"><span data-stu-id="6d3ed-124">Client</span></span><br/> | <span data-ttu-id="6d3ed-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d3ed-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6d3ed-126">Server</span><span class="sxs-lookup"><span data-stu-id="6d3ed-126">Server</span></span><br/> | <span data-ttu-id="6d3ed-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d3ed-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d3ed-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d3ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3ed-129">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="6d3ed-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6d3ed-130">eapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="6d3ed-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





