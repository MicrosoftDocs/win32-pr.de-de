---
title: Baseeapparameters Complex Type-Verbindungs Eigenschaften
description: Definiert das Platzhalter Element für den Methodentyp und die Methoden spezifische Konfiguration.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Baseeapparameters komplexer Typ EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106353408"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="09213-104">Baseeapparameters Complex Type-Verbindungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09213-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="09213-105">Der komplexe Typ **baseeapparameters** definiert das Platzhalter Element für den Methodentyp und die Methoden spezifische Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09213-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="09213-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09213-106">Child elements</span></span>



| <span data-ttu-id="09213-107">Element</span><span class="sxs-lookup"><span data-stu-id="09213-107">Element</span></span>                                                                            | <span data-ttu-id="09213-108">type</span><span class="sxs-lookup"><span data-stu-id="09213-108">Type</span></span>    | <span data-ttu-id="09213-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09213-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="09213-110">**type**</span><span class="sxs-lookup"><span data-stu-id="09213-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="09213-111">integer</span><span class="sxs-lookup"><span data-stu-id="09213-111">integer</span></span> | <span data-ttu-id="09213-112">Eine beliebige Schema Instanz ist hier zulässig.</span><span class="sxs-lookup"><span data-stu-id="09213-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="09213-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09213-113">Remarks</span></span>

<span data-ttu-id="09213-114">In **baseeapparameters** kann die-Methode die konstituierenden Elemente definieren.</span><span class="sxs-lookup"><span data-stu-id="09213-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="09213-115">Die-Methode führt auch eine Schema Validierung für die Elemente in **baseeapparameters** aus.</span><span class="sxs-lookup"><span data-stu-id="09213-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="09213-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09213-116">Requirements</span></span>



| <span data-ttu-id="09213-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09213-117">Requirement</span></span> | <span data-ttu-id="09213-118">Wert</span><span class="sxs-lookup"><span data-stu-id="09213-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09213-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09213-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09213-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09213-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09213-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09213-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09213-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09213-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09213-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09213-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09213-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="09213-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="09213-125">baseeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="09213-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





