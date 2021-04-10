---
title: Accept-Servername (Peer-extensionstype)-Element
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Accept-Servername (Peer-extensionstype)-Element
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Accept-Servername-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961478"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="e510b-105">Accept-Servername (Peer-extensionstype)-Element</span><span class="sxs-lookup"><span data-stu-id="e510b-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="e510b-106">Das Element "Accepted Servername **(Peer-extensionstype)** " gibt an, ob der Servername anhand der im Servername [**(servervalidationparameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegebenen Namens Zeichenfolge validiert wird.</span><span class="sxs-lookup"><span data-stu-id="e510b-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="e510b-107">Das Element " **Accept Servername** " wird vom Element " [**Peer Name extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="e510b-107">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e510b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e510b-108">Remarks</span></span>

<span data-ttu-id="e510b-109">Das Element " **Accept Servername** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="e510b-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e510b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e510b-110">Requirements</span></span>



| <span data-ttu-id="e510b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e510b-111">Requirement</span></span> | <span data-ttu-id="e510b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e510b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e510b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e510b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e510b-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e510b-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e510b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e510b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e510b-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e510b-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e510b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e510b-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e510b-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="e510b-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e510b-119">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="e510b-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="e510b-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="e510b-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e510b-121">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="e510b-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="e510b-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e510b-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e510b-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="e510b-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e510b-124">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="e510b-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e510b-125">mspeapconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="e510b-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





