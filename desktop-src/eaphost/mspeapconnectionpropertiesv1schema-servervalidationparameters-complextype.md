---
title: Komplexer servervalidationparameters-Typ (Peer)
description: Erfahren Sie mehr über den komplexen servervalidationparameters-Typ. Dieser Typ enthält Informationen zum Durchführen der Server Validierung. | Komplexer servervalidationparameters-Typ (Peer)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- Servervalidationparameters komplexer Typ EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961292"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="8d048-106">Komplexer servervalidationparameters-Typ (Peer)</span><span class="sxs-lookup"><span data-stu-id="8d048-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="8d048-107">Der komplexe Typ **servervalidationparameters** enthält Informationen zum Durchführen der Server Validierung.</span><span class="sxs-lookup"><span data-stu-id="8d048-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8d048-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d048-108">Child elements</span></span>



| <span data-ttu-id="8d048-109">Element</span><span class="sxs-lookup"><span data-stu-id="8d048-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="8d048-110">type</span><span class="sxs-lookup"><span data-stu-id="8d048-110">Type</span></span>        | <span data-ttu-id="8d048-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d048-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d048-112">**Disableuserpromptforservervalidation**</span><span class="sxs-lookup"><span data-stu-id="8d048-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="8d048-113">boolean</span><span class="sxs-lookup"><span data-stu-id="8d048-113">boolean</span></span>     | <span data-ttu-id="8d048-114">Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d048-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="8d048-115">Wenn [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) den Wert true hat, führt die Überprüfung des Servers ohne Benutzereingaben durch. Wenn die Überprüfung fehlschlägt, schlägt die Authentifizierung fehl.</span><span class="sxs-lookup"><span data-stu-id="8d048-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="8d048-116">Wenn [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8d048-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="8d048-117">Das [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d048-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="8d048-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="8d048-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="8d048-119">complexType</span><span class="sxs-lookup"><span data-stu-id="8d048-119">complextype</span></span> | <span data-ttu-id="8d048-120">Stellt eine Liste von Servern dar, denen der Client vertraut.</span><span class="sxs-lookup"><span data-stu-id="8d048-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="8d048-121">Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8d048-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="8d048-122">Das [**servernames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d048-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="8d048-123">**Treuhändrootca**</span><span class="sxs-lookup"><span data-stu-id="8d048-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="8d048-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="8d048-124">hexBinary</span></span>   | <span data-ttu-id="8d048-125">Zeichnet den Fingerabdruck der Stamm Zertifizierungsstellen (CAS) auf, die vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="8d048-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="8d048-126">Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="8d048-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="8d048-127">Das Element " [**treuhändrootca**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d048-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="8d048-128">Attributes</span><span class="sxs-lookup"><span data-stu-id="8d048-128">Attributes</span></span>



| <span data-ttu-id="8d048-129">Name</span><span class="sxs-lookup"><span data-stu-id="8d048-129">Name</span></span>                    | <span data-ttu-id="8d048-130">type</span><span class="sxs-lookup"><span data-stu-id="8d048-130">Type</span></span>    | <span data-ttu-id="8d048-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d048-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d048-132">Performservervalidation</span><span class="sxs-lookup"><span data-stu-id="8d048-132">PerformServerValidation</span></span> | <span data-ttu-id="8d048-133">boolean</span><span class="sxs-lookup"><span data-stu-id="8d048-133">boolean</span></span> | <span data-ttu-id="8d048-134">Windows 7 oder höher: gibt an, ob die Server Validierung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d048-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="8d048-135">Das [**performservervalidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d048-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8d048-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d048-136">Requirements</span></span>



| <span data-ttu-id="8d048-137">Role</span><span class="sxs-lookup"><span data-stu-id="8d048-137">Role</span></span> | <span data-ttu-id="8d048-138">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="8d048-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="8d048-139">Client</span><span class="sxs-lookup"><span data-stu-id="8d048-139">Client</span></span><br/> | <span data-ttu-id="8d048-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d048-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8d048-141">Server</span><span class="sxs-lookup"><span data-stu-id="8d048-141">Server</span></span><br/> | <span data-ttu-id="8d048-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d048-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d048-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d048-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d048-144">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="8d048-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8d048-145">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="8d048-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="8d048-146">komplexe mspeapconnectionpropertiesv1-Schema Typen</span><span class="sxs-lookup"><span data-stu-id="8d048-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8d048-147">**Akzeptservername**</span><span class="sxs-lookup"><span data-stu-id="8d048-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





