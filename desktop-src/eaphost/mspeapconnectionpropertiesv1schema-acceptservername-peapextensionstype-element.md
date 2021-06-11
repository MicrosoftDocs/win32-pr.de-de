---
title: AcceptServerName (PeapExtensionsType) -Element (EAPHost)
description: Das AcceptServerName-Element (PeapExtensionsType) gibt an, ob der Servername anhand der Namenszeichenfolge überprüft wird, die im Schema mspeapconnectionpropertiesv1 in serverNames angegeben ist.
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- Element EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989095"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="023f4-104">AcceptServerName (PeapExtensionsType) -Element (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="023f4-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="023f4-105">Das **AcceptServerName -Element (PeapExtensionsType)** gibt an, ob der Servername anhand der Im [**ServerNames -Element (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) angegebenen Namenszeichenfolge überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="023f4-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="023f4-106">Das -Element wird durch das [**PeapExtensionsType-Element**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="023f4-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="023f4-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="023f4-107">Remarks</span></span>

<span data-ttu-id="023f4-108">Das **AcceptServerName-Element** ist optional.</span><span class="sxs-lookup"><span data-stu-id="023f4-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="023f4-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="023f4-109">Requirements</span></span>



| <span data-ttu-id="023f4-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="023f4-110">Requirement</span></span> | <span data-ttu-id="023f4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="023f4-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="023f4-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="023f4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="023f4-113">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="023f4-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="023f4-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="023f4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="023f4-115">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="023f4-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="023f4-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="023f4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="023f4-117">**Definitionskontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="023f4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="023f4-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="023f4-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="023f4-119">**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**</span><span class="sxs-lookup"><span data-stu-id="023f4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="023f4-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="023f4-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="023f4-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="023f4-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="023f4-122">EAPHost und Legacyschema</span><span class="sxs-lookup"><span data-stu-id="023f4-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="023f4-123">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="023f4-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="023f4-124">mspeapconnectionpropertiesv1-Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="023f4-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="023f4-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="023f4-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





