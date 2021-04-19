---
title: Disableuserpromptforservervalidation-Element (Peer-APP)
description: Erfahren Sie mehr über das disableuserpromptforservervalidation (servervalidationparameters)-Element. Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll. | Disableuserpromptforservervalidation-Element (Peer-APP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- Disableuserpromptforservervalidation-Element EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363920"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="b3de5-106">Disableuserpromptforservervalidation (servervalidationparameters)-Element (Peer-APP)</span><span class="sxs-lookup"><span data-stu-id="b3de5-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="b3de5-107">Das **disableuserpromptforservervalidation (servervalidationparameters)** -Element gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3de5-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="b3de5-108">Wenn " **disableuserpromptforservervalidation** " den Wert "true" hat, führt EAP-TLS die Server Validierung ohne Benutzereingaben aus. Wenn die Überprüfung fehlschlägt, schlägt EAP-TLS die Authentifizierung fehl.</span><span class="sxs-lookup"><span data-stu-id="b3de5-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="b3de5-109">Wenn **disableuserpromptforservervalidation** den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle (Root Certificate Authority, ca) aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b3de5-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="b3de5-110">Das **disableuserpromptforservervalidation** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="b3de5-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="b3de5-111">Das **disableuserpromptforservervalidation** -Element wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="b3de5-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3de5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3de5-112">Requirements</span></span>



| <span data-ttu-id="b3de5-113">Role</span><span class="sxs-lookup"><span data-stu-id="b3de5-113">Role</span></span> | <span data-ttu-id="b3de5-114">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="b3de5-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b3de5-115">Client</span><span class="sxs-lookup"><span data-stu-id="b3de5-115">Client</span></span><br/> | <span data-ttu-id="b3de5-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3de5-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3de5-117">Server</span><span class="sxs-lookup"><span data-stu-id="b3de5-117">Server</span></span><br/> | <span data-ttu-id="b3de5-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3de5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3de5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3de5-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3de5-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="b3de5-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3de5-121">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="b3de5-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="b3de5-122">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="b3de5-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3de5-123">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="b3de5-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="b3de5-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b3de5-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b3de5-125">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="b3de5-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b3de5-126">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="b3de5-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b3de5-127">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="b3de5-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





