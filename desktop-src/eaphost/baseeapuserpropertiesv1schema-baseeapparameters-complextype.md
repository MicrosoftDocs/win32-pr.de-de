---
title: 'Basieeapparameters komplexer Typ: Benutzereigenschaften'
description: Definiert das Element, das die ausgewählte Legacy Methode und die Methoden spezifischen Anmelde Informationen angegeben hat.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106365360"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="a9da5-104">Basieeapparameters komplexer Typ: Benutzereigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9da5-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="a9da5-105">Der komplexe Typ **baseeapparameters** definiert das Element, das die ausgewählte Legacy Methode und die Methoden spezifischen Anmelde Informationen angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a9da5-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="a9da5-106">Die-Methode kann die konstituierenden Elemente innerhalb von **baseeapparameters** definieren. die-Methode führt auch eine Schema Validierung für die Elemente in **baseeapparameters** aus.</span><span class="sxs-lookup"><span data-stu-id="a9da5-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="a9da5-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9da5-107">Child elements</span></span>



| <span data-ttu-id="a9da5-108">Element</span><span class="sxs-lookup"><span data-stu-id="a9da5-108">Element</span></span>                                                                      | <span data-ttu-id="a9da5-109">type</span><span class="sxs-lookup"><span data-stu-id="a9da5-109">Type</span></span>    | <span data-ttu-id="a9da5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9da5-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9da5-111">**type**</span><span class="sxs-lookup"><span data-stu-id="a9da5-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="a9da5-112">integer</span><span class="sxs-lookup"><span data-stu-id="a9da5-112">integer</span></span> | <span data-ttu-id="a9da5-113">Definiert das Platzhalter Element für den ausgewählten Methodentyp und die Methoden spezifischen Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="a9da5-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="a9da5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9da5-114">Requirements</span></span>



| <span data-ttu-id="a9da5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9da5-115">Requirement</span></span> | <span data-ttu-id="a9da5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a9da5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9da5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9da5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9da5-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9da5-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9da5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9da5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9da5-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9da5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9da5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9da5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9da5-122">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="a9da5-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a9da5-123">baseeapuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="a9da5-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





