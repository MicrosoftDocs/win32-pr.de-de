---
title: Eaptype-Element (mspeapconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionproperties-Schema. Für mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368278"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="abab0-105">Eaptype-Element (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="abab0-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="abab0-106">Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionproperties](baseeapconnectionpropertiesv1schema-schema.md) -Schema.</span><span class="sxs-lookup"><span data-stu-id="abab0-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="abab0-107">Dieses abgeleitete **eaptype** -Element enthält die folgenden Elemente: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**identityprivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**enablequarantäne-Prüfungen**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) und [**peapextensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="abab0-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="abab0-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abab0-108">Child elements</span></span>



| <span data-ttu-id="abab0-109">Element</span><span class="sxs-lookup"><span data-stu-id="abab0-109">Element</span></span>                                                                                                     | <span data-ttu-id="abab0-110">type</span><span class="sxs-lookup"><span data-stu-id="abab0-110">Type</span></span>                                                                                                            | <span data-ttu-id="abab0-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abab0-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abab0-112">**EAP**</span><span class="sxs-lookup"><span data-stu-id="abab0-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="abab0-113">Beschreibt die innere-Methode und die-Methoden Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="abab0-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="abab0-114">Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="abab0-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="abab0-115">Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element false ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="abab0-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="abab0-116">**Enablequarantäne-Prüfungen**</span><span class="sxs-lookup"><span data-stu-id="abab0-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="abab0-117">boolean</span><span class="sxs-lookup"><span data-stu-id="abab0-117">boolean</span></span>                                                                                                         | <span data-ttu-id="abab0-118">Gibt an, ob Netzwerk Zugriffsschutz (NAP)-Überprüfungen durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abab0-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="abab0-119">Wenn das [**enablequarantäne**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) -Element auf "true" festgestellt wird, werden NAP-Überprüfungen durchgeführt. Wenn der Wert false ist, werden keine NAP-Überprüfungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="abab0-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="abab0-120">Das [**enablequarantäne inechecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="abab0-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="abab0-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="abab0-122">boolean</span><span class="sxs-lookup"><span data-stu-id="abab0-122">boolean</span></span>                                                                                                         | <span data-ttu-id="abab0-123">Gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abab0-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="abab0-124">Wenn das [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) -Element "true" ist, versucht die Peer-APP, eine schnelle erneute Verbindungs Herstellung auszuführen. der Wert false gibt an, dass die vollständige Authentifizierung von Peer-App</span><span class="sxs-lookup"><span data-stu-id="abab0-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="abab0-125">Das [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="abab0-126">**Identityprivacy**</span><span class="sxs-lookup"><span data-stu-id="abab0-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="abab0-127">**Identityprivacyparameters**</span><span class="sxs-lookup"><span data-stu-id="abab0-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="abab0-128">Windows 7 oder höher: gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="abab0-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="abab0-129">Das [**identityprivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="abab0-130">**Innereapoptional**</span><span class="sxs-lookup"><span data-stu-id="abab0-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="abab0-131">boolean</span><span class="sxs-lookup"><span data-stu-id="abab0-131">boolean</span></span>                                                                                                         | <span data-ttu-id="abab0-132">Gibt an, ob Gast Zugriff durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abab0-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="abab0-133">Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein und die innere Methode und die zugehörige Konfiguration beschreiben. Wenn der Wert false ist, führt der Peer-Agent den Gast Zugriff aus.</span><span class="sxs-lookup"><span data-stu-id="abab0-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="abab0-134">Das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="abab0-135">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="abab0-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="abab0-136">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="abab0-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="abab0-137">Das Element " [**Peer-Erweiterungen**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) " ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="abab0-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="abab0-138">Das Element " [**Peer-Extensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="abab0-139">**Requirecryptobinding**</span><span class="sxs-lookup"><span data-stu-id="abab0-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="abab0-140">boolean</span><span class="sxs-lookup"><span data-stu-id="abab0-140">boolean</span></span>                                                                                                         | <span data-ttu-id="abab0-141">Gibt an, ob die Authentifizierung mit Servern durch die kryptobindung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="abab0-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="abab0-142">Wenn das Element " [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) " den Wert "true" hat, wird die Authentifizierung mit Servern durchführt, die cryptobinding nicht unterstützen. Wenn der Wert false ist, wird die Authentifizierung nur bei Servern durchführt, die cryptobinding unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abab0-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="abab0-143">Das Element " [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="abab0-144">**Server Validierung**</span><span class="sxs-lookup"><span data-stu-id="abab0-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="abab0-145">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="abab0-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="abab0-146">Enthält Informationen zum Durchführen der Server Validierung.</span><span class="sxs-lookup"><span data-stu-id="abab0-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="abab0-147">Das [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="abab0-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="abab0-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abab0-148">Requirements</span></span>



| <span data-ttu-id="abab0-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abab0-149">Requirement</span></span> | <span data-ttu-id="abab0-150">Wert</span><span class="sxs-lookup"><span data-stu-id="abab0-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="abab0-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abab0-151">Minimum supported client</span></span><br/> | <span data-ttu-id="abab0-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abab0-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="abab0-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abab0-153">Minimum supported server</span></span><br/> | <span data-ttu-id="abab0-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abab0-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abab0-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abab0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abab0-156">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="abab0-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="abab0-157">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="abab0-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="abab0-158">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="abab0-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





