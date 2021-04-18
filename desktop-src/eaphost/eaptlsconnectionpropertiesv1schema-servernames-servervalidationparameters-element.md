---
title: Server Ames (servervalidationparameters)-Element (TLS)
description: Erfahren Sie mehr über das servernames (servervalidationparameters)-Element. Dieses Element stellt eine Liste von durch Semikolons getrennten Servernamen dar. | Server Ames (servervalidationparameters)-Element (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Servernames-Element EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361168"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="456e0-106">Server Ames (servervalidationparameters)-Element (TLS)</span><span class="sxs-lookup"><span data-stu-id="456e0-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="456e0-107">Das Server **Ames (servervalidationparameters)** -Element stellt eine Liste von durch Semikolons getrennten Servernamen dar.</span><span class="sxs-lookup"><span data-stu-id="456e0-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="456e0-108">Das **servernames** -Element wird durch den komplexen [**servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="456e0-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="456e0-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="456e0-109">Remarks</span></span>

<span data-ttu-id="456e0-110">Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="456e0-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="456e0-111">Das **servernames** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="456e0-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="456e0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="456e0-112">Requirements</span></span>



| <span data-ttu-id="456e0-113">Role</span><span class="sxs-lookup"><span data-stu-id="456e0-113">Role</span></span> | <span data-ttu-id="456e0-114">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="456e0-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="456e0-115">Client</span><span class="sxs-lookup"><span data-stu-id="456e0-115">Client</span></span><br/> | <span data-ttu-id="456e0-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456e0-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="456e0-117">Server</span><span class="sxs-lookup"><span data-stu-id="456e0-117">Server</span></span><br/> | <span data-ttu-id="456e0-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456e0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="456e0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="456e0-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="456e0-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="456e0-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="456e0-121">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="456e0-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="456e0-122">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="456e0-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="456e0-123">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="456e0-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="456e0-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="456e0-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="456e0-125">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="456e0-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="456e0-126">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="456e0-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="456e0-127">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="456e0-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





