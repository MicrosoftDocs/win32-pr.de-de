---
title: Komplexer Dateityp "Peer apextensionstype" (Verbindungs Eigenschaften)
description: Erfahren Sie mehr über den komplexen Typ "apapextensionstype". Dieser Typ ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Komplexer Typ von "etapextensionstype" EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316485"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="9e588-105">Komplexer Dateityp "Peer apextensionstype" (Verbindungs Eigenschaften)</span><span class="sxs-lookup"><span data-stu-id="9e588-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="9e588-106">Der komplexe Typ " **Peer apextensionstype** " ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="9e588-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="9e588-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e588-107">Remarks</span></span>

<span data-ttu-id="9e588-108">Der komplexe Typ " **Peer apextensionstype** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="9e588-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e588-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e588-109">Requirements</span></span>



| <span data-ttu-id="9e588-110">Role</span><span class="sxs-lookup"><span data-stu-id="9e588-110">Role</span></span> | <span data-ttu-id="9e588-111">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="9e588-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="9e588-112">Client</span><span class="sxs-lookup"><span data-stu-id="9e588-112">Client</span></span><br/> | <span data-ttu-id="9e588-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e588-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e588-114">Server</span><span class="sxs-lookup"><span data-stu-id="9e588-114">Server</span></span><br/> | <span data-ttu-id="9e588-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e588-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e588-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e588-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e588-117">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="9e588-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9e588-118">mspeapuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="9e588-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





