---
title: Eaptype-Element (eaptlsuserpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106362112"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="e4a24-105">Eaptype-Element (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="e4a24-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="e4a24-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapuserpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="e4a24-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
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

## <a name="child-elements"></a><span data-ttu-id="e4a24-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e4a24-107">Child elements</span></span>



| <span data-ttu-id="e4a24-108">Element</span><span class="sxs-lookup"><span data-stu-id="e4a24-108">Element</span></span>                                                                   | <span data-ttu-id="e4a24-109">type</span><span class="sxs-lookup"><span data-stu-id="e4a24-109">Type</span></span>      | <span data-ttu-id="e4a24-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4a24-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4a24-111">**Benutzername**</span><span class="sxs-lookup"><span data-stu-id="e4a24-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="e4a24-112">Erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4a24-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="e4a24-113">Wenn das [**username**](eaptlsuserpropertiesv1schema-username-element.md) -Element nicht vorhanden ist, verwendet EAP-TLS den Namen in dem Zertifikat, auf das im [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e4a24-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="e4a24-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="e4a24-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="e4a24-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e4a24-115">hexBinary</span></span> | <span data-ttu-id="e4a24-116">Bezieht sich auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4a24-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="e4a24-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4a24-117">Remarks</span></span>

<span data-ttu-id="e4a24-118">Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="e4a24-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="e4a24-119">Das **processContents** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e4a24-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a24-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a24-120">Requirements</span></span>



| <span data-ttu-id="e4a24-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4a24-121">Requirement</span></span> | <span data-ttu-id="e4a24-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e4a24-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4a24-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4a24-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a24-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4a24-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4a24-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4a24-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a24-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4a24-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4a24-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4a24-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a24-128">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="e4a24-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e4a24-129">eaptlsuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="e4a24-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





