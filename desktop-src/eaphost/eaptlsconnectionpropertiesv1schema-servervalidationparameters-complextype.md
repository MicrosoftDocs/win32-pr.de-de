---
title: Servervalidationparameters komplexer Typ (TLS)
description: Erfahren Sie mehr über den komplexen servervalidationparameters-Typ. Dieser Typ enthält Informationen zum Durchführen der Server Validierung. | Servervalidationparameters komplexer Typ (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
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
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351884"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="529fe-106">Servervalidationparameters komplexer Typ (TLS)</span><span class="sxs-lookup"><span data-stu-id="529fe-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="529fe-107">Der komplexe Typ **servervalidationparameters** enthält Informationen zum Durchführen der Server Validierung.</span><span class="sxs-lookup"><span data-stu-id="529fe-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="529fe-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="529fe-108">Child elements</span></span>



| <span data-ttu-id="529fe-109">Element</span><span class="sxs-lookup"><span data-stu-id="529fe-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="529fe-110">type</span><span class="sxs-lookup"><span data-stu-id="529fe-110">Type</span></span>      | <span data-ttu-id="529fe-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="529fe-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="529fe-112">**Disableuserpromptforservervalidation**</span><span class="sxs-lookup"><span data-stu-id="529fe-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="529fe-113">boolean</span><span class="sxs-lookup"><span data-stu-id="529fe-113">boolean</span></span>   | <span data-ttu-id="529fe-114">Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="529fe-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="529fe-115">Wenn " [**disableuserpromptforservervalidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) " den Wert "true" hat, führt EAP-TLS die Server Validierung ohne Benutzereingaben aus. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl.</span><span class="sxs-lookup"><span data-stu-id="529fe-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="529fe-116">Wenn [**disableuserpromptforservervalidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle (Root Certificate Authority, ca) aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="529fe-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="529fe-117">Das [**disableuserpromptforservervalidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="529fe-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="529fe-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="529fe-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="529fe-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="529fe-119">string</span></span>    | <span data-ttu-id="529fe-120">Stellt eine Liste von Servern dar, denen der Client vertraut.</span><span class="sxs-lookup"><span data-stu-id="529fe-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="529fe-121">Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="529fe-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="529fe-122">Das [**servernames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="529fe-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="529fe-123">**Treuhändrootca**</span><span class="sxs-lookup"><span data-stu-id="529fe-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="529fe-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="529fe-124">hexBinary</span></span> | <span data-ttu-id="529fe-125">Zeichnet den Fingerabdruck der Stamm Zertifizierungsstellen (CAS) auf, die vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="529fe-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="529fe-126">Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="529fe-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="529fe-127">Das Element " [**treuhändrootca**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) " ist optional.</span><span class="sxs-lookup"><span data-stu-id="529fe-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="529fe-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="529fe-128">Requirements</span></span>



| <span data-ttu-id="529fe-129">Role</span><span class="sxs-lookup"><span data-stu-id="529fe-129">Role</span></span> | <span data-ttu-id="529fe-130">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="529fe-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="529fe-131">Client</span><span class="sxs-lookup"><span data-stu-id="529fe-131">Client</span></span><br/> | <span data-ttu-id="529fe-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="529fe-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="529fe-133">Server</span><span class="sxs-lookup"><span data-stu-id="529fe-133">Server</span></span><br/> | <span data-ttu-id="529fe-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="529fe-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="529fe-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="529fe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="529fe-136">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="529fe-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="529fe-137">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="529fe-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="529fe-138">komplexe eaptlsconnectionpropertiesv1-Schema Typen</span><span class="sxs-lookup"><span data-stu-id="529fe-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





