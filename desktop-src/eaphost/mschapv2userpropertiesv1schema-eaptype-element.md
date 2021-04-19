---
title: Eaptype-Element (mschapv2userpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapuserpropertiesv1-Schema. Für mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106355074"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="11bbd-105">Eaptype-Element (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="11bbd-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="11bbd-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapuserpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="11bbd-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
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

## <a name="child-elements"></a><span data-ttu-id="11bbd-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11bbd-107">Child elements</span></span>



| <span data-ttu-id="11bbd-108">Element</span><span class="sxs-lookup"><span data-stu-id="11bbd-108">Element</span></span>                                                                           | <span data-ttu-id="11bbd-109">type</span><span class="sxs-lookup"><span data-stu-id="11bbd-109">Type</span></span>   | <span data-ttu-id="11bbd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11bbd-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11bbd-111">**Benutzername**</span><span class="sxs-lookup"><span data-stu-id="11bbd-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="11bbd-112">Identifiziert den Benutzer, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="11bbd-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="11bbd-113">Wenn dieses Element nicht vorhanden ist, wird der Benutzername aus Winlogon abgerufen.</span><span class="sxs-lookup"><span data-stu-id="11bbd-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="11bbd-114">Das [**username**](mschapv2userpropertiesv1schema-username-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="11bbd-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="11bbd-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="11bbd-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="11bbd-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11bbd-116">string</span></span> | <span data-ttu-id="11bbd-117">Identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="11bbd-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="11bbd-118">Wenn dieses Element nicht vorhanden ist, wird die Domäne von Winlogon verwendet.</span><span class="sxs-lookup"><span data-stu-id="11bbd-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="11bbd-119">Das [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="11bbd-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="11bbd-120">**Anmelden**</span><span class="sxs-lookup"><span data-stu-id="11bbd-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="11bbd-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="11bbd-121">string</span></span> | <span data-ttu-id="11bbd-122">Identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="11bbd-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="11bbd-123">Wenn dieses Element nicht vorhanden ist, wird der Kenn Wort Hash von Winlogon abgerufen.</span><span class="sxs-lookup"><span data-stu-id="11bbd-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="11bbd-124">Das [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="11bbd-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="11bbd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11bbd-125">Remarks</span></span>

<span data-ttu-id="11bbd-126">Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="11bbd-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="11bbd-127">Das **processContents** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="11bbd-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bbd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11bbd-128">Requirements</span></span>



| <span data-ttu-id="11bbd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11bbd-129">Requirement</span></span> | <span data-ttu-id="11bbd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="11bbd-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11bbd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11bbd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="11bbd-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11bbd-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11bbd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11bbd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="11bbd-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11bbd-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11bbd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11bbd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bbd-136">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="11bbd-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="11bbd-137">mschapv2userpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="11bbd-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





