---
title: Server Ames (servervalidationparameters)-Element (Peer Name)
description: Erfahren Sie mehr über das servernames (servervalidationparameters)-Element. Dieses Element stellt eine Liste von durch Semikolons getrennten Servernamen dar. | Server Ames (servervalidationparameters)-Element (Peer Name)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354304"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="bb81d-106">Server Ames (servervalidationparameters)-Element (Peer Name)</span><span class="sxs-lookup"><span data-stu-id="bb81d-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="bb81d-107">Das Server **Ames (servervalidationparameters)** -Element stellt eine Liste von durch Semikolons getrennten Servernamen dar.</span><span class="sxs-lookup"><span data-stu-id="bb81d-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="bb81d-108">Das **servernames** -Element wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="bb81d-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb81d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb81d-109">Remarks</span></span>

<span data-ttu-id="bb81d-110">Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bb81d-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="bb81d-111">Das **servernames** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bb81d-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb81d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb81d-112">Requirements</span></span>



| <span data-ttu-id="bb81d-113">Role</span><span class="sxs-lookup"><span data-stu-id="bb81d-113">Role</span></span> | <span data-ttu-id="bb81d-114">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="bb81d-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="bb81d-115">Client</span><span class="sxs-lookup"><span data-stu-id="bb81d-115">Client</span></span><br/> | <span data-ttu-id="bb81d-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb81d-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb81d-117">Server</span><span class="sxs-lookup"><span data-stu-id="bb81d-117">Server</span></span><br/> | <span data-ttu-id="bb81d-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb81d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb81d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb81d-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb81d-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="bb81d-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb81d-121">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="bb81d-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="bb81d-122">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="bb81d-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb81d-123">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="bb81d-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="bb81d-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bb81d-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bb81d-125">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="bb81d-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bb81d-126">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="bb81d-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bb81d-127">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="bb81d-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





