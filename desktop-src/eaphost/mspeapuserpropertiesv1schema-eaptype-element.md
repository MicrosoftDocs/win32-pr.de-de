---
title: Eaptype-Element (mspeapuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Eaptype-Element EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368280"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="3b657-105">Eaptype-Element (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="3b657-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="3b657-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapuserpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="3b657-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="3b657-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b657-107">Child elements</span></span>



| <span data-ttu-id="3b657-108">Element</span><span class="sxs-lookup"><span data-stu-id="3b657-108">Element</span></span>                                                                               | <span data-ttu-id="3b657-109">type</span><span class="sxs-lookup"><span data-stu-id="3b657-109">Type</span></span>                                                                                      | <span data-ttu-id="3b657-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b657-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b657-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="3b657-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="3b657-112">Das [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) -Element identifiziert die innere Methode und die Anmelde Informationen, die mit dieser Methode verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b657-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="3b657-113">Wenn die Peer-Konfiguration für den Zugriff auf den Peer-Gast Zugriff konfiguriert ist, ist dieses Element nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3b657-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="3b657-114">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="3b657-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="3b657-115">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="3b657-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="3b657-116">Das Element " [**Peer-Erweiterungen**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) " ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="3b657-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="3b657-117">Das Element " [**Peer-Extensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="3b657-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3b657-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b657-118">Requirements</span></span>



| <span data-ttu-id="3b657-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b657-119">Requirement</span></span> | <span data-ttu-id="3b657-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3b657-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b657-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b657-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b657-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b657-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b657-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b657-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b657-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b657-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b657-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b657-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b657-126">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="3b657-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3b657-127">mspeapuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="3b657-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





