---
title: Komplexer PeapExtensionsTypeV2-Typ
description: Erfahren Sie mehr über den komplexen PeapExtensionsTypeV2-Typ. Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949128"
---
# <a name="peapextensionstypev2-complex-type"></a><span data-ttu-id="9bf63-104">Komplexer PeapExtensionsTypeV2-Typ</span><span class="sxs-lookup"><span data-stu-id="9bf63-104">PeapExtensionsTypeV2 Complex Type</span></span>

<span data-ttu-id="9bf63-105">Der komplexe Typ " **PeapExtensionsTypeV2** " ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="9bf63-105">The **PeapExtensionsTypeV2** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="9bf63-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bf63-106">Remarks</span></span>

<span data-ttu-id="9bf63-107">Das **PeapExtensionsTypeV2** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9bf63-107">The **PeapExtensionsTypeV2** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bf63-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bf63-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf63-109">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="9bf63-109">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9bf63-110">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="9bf63-110">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="9bf63-111">komplexe mspeapconnectionpropertiesv2-Typen</span><span class="sxs-lookup"><span data-stu-id="9bf63-111">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9bf63-112">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="9bf63-112">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




