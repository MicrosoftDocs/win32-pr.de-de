---
title: Eaptype-Element (mschapv2connectionpropertiesv1schema)
description: Ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionpropertiesv1-Schema. Dies ist das oberste Element, das im config-Element des eaphostconfig-Schemas angezeigt wird.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106367176"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="6ce4c-105">Eaptype-Element (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="6ce4c-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="6ce4c-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [eaptype](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="6ce4c-107">Dies ist das oberste Element, das im config-Element des [eaphostconfig](eaphostconfigschema-elements.md) -Schemas angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="6ce4c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ce4c-108">Child elements</span></span>



| <span data-ttu-id="6ce4c-109">Element</span><span class="sxs-lookup"><span data-stu-id="6ce4c-109">Element</span></span>                                                                                                       | <span data-ttu-id="6ce4c-110">type</span><span class="sxs-lookup"><span data-stu-id="6ce4c-110">Type</span></span>    | <span data-ttu-id="6ce4c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ce4c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ce4c-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="6ce4c-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="6ce4c-113">boolean</span><span class="sxs-lookup"><span data-stu-id="6ce4c-113">boolean</span></span> | <span data-ttu-id="6ce4c-114">Steuert die Verwendung der winlogin-Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="6ce4c-115">Wenn der Wert true ist, erhält der EAP-MS-CHAPv2 Anmelde Informationen von Winlogon.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="6ce4c-116">Wenn der Wert false ist, erhält EAP MS-CHAPv2 Anmelde Informationen vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="6ce4c-117">Das [**usewinlogon-Anmelde Informationen-Element (eaptype)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6ce4c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ce4c-118">Remarks</span></span>

<span data-ttu-id="6ce4c-119">Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="6ce4c-120">Das **processContents** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ce4c-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce4c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ce4c-121">Requirements</span></span>



| <span data-ttu-id="6ce4c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ce4c-122">Requirement</span></span> | <span data-ttu-id="6ce4c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6ce4c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ce4c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ce4c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ce4c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ce4c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ce4c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ce4c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ce4c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ce4c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ce4c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ce4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce4c-129">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="6ce4c-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6ce4c-130">mschapv2connectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="6ce4c-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





