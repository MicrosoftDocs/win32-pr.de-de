---
description: Definiert den Abschnitt des Instrumentierungs Manifests, mit dem der Anbieter und die von Ihnen bereitgestellten Indikatoren identifiziert werden.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: komplexer Typ der Leistungsindikatoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959755"
---
# <a name="counters-complex-type"></a><span data-ttu-id="8e6de-103">komplexer Typ der Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="8e6de-103">counters Complex Type</span></span>

<span data-ttu-id="8e6de-104">Definiert den Abschnitt des Instrumentierungs Manifests, mit dem der Anbieter und die von Ihnen bereitgestellten Indikatoren identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8e6de-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8e6de-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e6de-105">Child elements</span></span>



| <span data-ttu-id="8e6de-106">Element</span><span class="sxs-lookup"><span data-stu-id="8e6de-106">Element</span></span>      | <span data-ttu-id="8e6de-107">type</span><span class="sxs-lookup"><span data-stu-id="8e6de-107">Type</span></span>                                                               | <span data-ttu-id="8e6de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e6de-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8e6de-109">**ab**</span><span class="sxs-lookup"><span data-stu-id="8e6de-109">**provider**</span></span> | [<span data-ttu-id="8e6de-110">**man: Provider**</span><span class="sxs-lookup"><span data-stu-id="8e6de-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="8e6de-111">Identifiziert einen Anbieter, der Leistungsindikatoren bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8e6de-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="8e6de-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="8e6de-112">Attributes</span></span>



| <span data-ttu-id="8e6de-113">Name</span><span class="sxs-lookup"><span data-stu-id="8e6de-113">Name</span></span>          | <span data-ttu-id="8e6de-114">type</span><span class="sxs-lookup"><span data-stu-id="8e6de-114">Type</span></span> | <span data-ttu-id="8e6de-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e6de-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="8e6de-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="8e6de-116">schemaVersion</span></span> |      | <span data-ttu-id="8e6de-117">Die Version des Schemas, das zum Schreiben des Manifests verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e6de-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8e6de-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e6de-118">Requirements</span></span>



| <span data-ttu-id="8e6de-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e6de-119">Requirement</span></span> | <span data-ttu-id="8e6de-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8e6de-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e6de-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e6de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e6de-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e6de-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e6de-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e6de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e6de-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e6de-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e6de-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e6de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e6de-126">**Ener**</span><span class="sxs-lookup"><span data-stu-id="8e6de-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

