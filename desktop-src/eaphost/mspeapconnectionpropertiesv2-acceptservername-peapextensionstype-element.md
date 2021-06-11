---
title: AcceptServerName (PeapExtensionsType)-Element
description: Das AcceptServerName -Element (PeapExtensionsType) gibt an, ob der Servername anhand der Namenszeichenfolge überprüft wird, die im Schema mspeapconnectionpropertiesv2 in ServerNames angegeben ist.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- AcceptServerName-Element EAPHost
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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989475"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="06f5c-104">AcceptServerName (PeapExtensionsType)-Element</span><span class="sxs-lookup"><span data-stu-id="06f5c-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="06f5c-105">Das **AcceptServerName -Element (PeapExtensionsType)** gibt an, ob der Servername anhand der Im [**ServerNames -Element (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) angegebenen Namenszeichenfolge überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="06f5c-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="06f5c-106">Das **AcceptServerName-Element** wird durch das [**PeapExtensionsType-Element**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="06f5c-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="06f5c-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06f5c-107">Remarks</span></span>

<span data-ttu-id="06f5c-108">Das **AcceptServerName-Element** ist optional.</span><span class="sxs-lookup"><span data-stu-id="06f5c-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f5c-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="06f5c-109">Requirements</span></span>



| <span data-ttu-id="06f5c-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06f5c-110">Requirement</span></span> | <span data-ttu-id="06f5c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="06f5c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="06f5c-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06f5c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="06f5c-113">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06f5c-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="06f5c-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06f5c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="06f5c-115">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06f5c-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06f5c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06f5c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="06f5c-117">**Definitionskontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="06f5c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="06f5c-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="06f5c-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="06f5c-119">**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**</span><span class="sxs-lookup"><span data-stu-id="06f5c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="06f5c-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="06f5c-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="06f5c-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="06f5c-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="06f5c-122">EAPHost und Legacyschema</span><span class="sxs-lookup"><span data-stu-id="06f5c-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="06f5c-123">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="06f5c-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="06f5c-124">mspeapconnectionpropertiesv2-Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="06f5c-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





