---
title: Eaptype-Element (eaptlsconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionproperties-Schema. Für eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106358189"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="bec70-105">Eaptype-Element (eaptlsconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="bec70-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="bec70-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionproperties](baseeapconnectionpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="bec70-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="bec70-107">Dieses abgeleitete **eaptype** -Element enthält die folgenden Elemente: " [**kredentialssource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)", " [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)", " [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)", " [**performservervalidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md)", " [**Accepted Server**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)Name" und "[**tlsextensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)".</span><span class="sxs-lookup"><span data-stu-id="bec70-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="bec70-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bec70-108">Child elements</span></span>



| <span data-ttu-id="bec70-109">Element</span><span class="sxs-lookup"><span data-stu-id="bec70-109">Element</span></span>                                                                                                                               | <span data-ttu-id="bec70-110">type</span><span class="sxs-lookup"><span data-stu-id="bec70-110">Type</span></span>                                                                                                              | <span data-ttu-id="bec70-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec70-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bec70-112">**extendedtls: performservervalidation**</span><span class="sxs-lookup"><span data-stu-id="bec70-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="bec70-113">Windows 7 und höher: gibt an, ob die Server Validierung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bec70-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="bec70-114">**extendedtls: akzeptservername**</span><span class="sxs-lookup"><span data-stu-id="bec70-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="bec70-115">Windows 7 und höher: gibt an, ob der Name eines Servers gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="bec70-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bec70-116">**extendedtls: tlsextensions**</span><span class="sxs-lookup"><span data-stu-id="bec70-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="bec70-117">Windows 7 und höher: ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="bec70-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="bec70-118">**"Kredentialssource"**</span><span class="sxs-lookup"><span data-stu-id="bec70-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="bec70-119">**"Kredentialssourceparameters"**</span><span class="sxs-lookup"><span data-stu-id="bec70-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="bec70-120">Enthält Informationen zum Speicherort des EAP-TLS-Zertifikats (Transport Level Security).</span><span class="sxs-lookup"><span data-stu-id="bec70-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="bec70-121">Das Element " [**kredentialssource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="bec70-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="bec70-122">**Differenentusername**</span><span class="sxs-lookup"><span data-stu-id="bec70-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="bec70-123">boolean</span><span class="sxs-lookup"><span data-stu-id="bec70-123">boolean</span></span>                                                                                                           | <span data-ttu-id="bec70-124">Bestimmt, welcher Benutzername von EAP-TLS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bec70-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="bec70-125">Wenn das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element **true** ist, sollte EAP-TLS einen anderen Benutzernamen als den Namen verwenden, der im Zertifikat angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bec70-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="bec70-126">Wenn das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element **false** ist, verwendet EAP-TLS den Benutzernamen, der im Zertifikat angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bec70-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="bec70-127">Das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bec70-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="bec70-128">**Server Validierung**</span><span class="sxs-lookup"><span data-stu-id="bec70-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="bec70-129">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="bec70-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="bec70-130">Enthält Informationen zum Durchführen der Server Validierung.</span><span class="sxs-lookup"><span data-stu-id="bec70-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="bec70-131">Das [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bec70-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="bec70-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bec70-132">Requirements</span></span>



| <span data-ttu-id="bec70-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bec70-133">Requirement</span></span> | <span data-ttu-id="bec70-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bec70-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bec70-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bec70-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bec70-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bec70-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bec70-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bec70-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bec70-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bec70-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bec70-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bec70-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec70-140">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="bec70-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bec70-141">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="bec70-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bec70-142">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="bec70-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





