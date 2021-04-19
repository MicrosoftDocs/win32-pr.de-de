---
title: Accept Servername (papextensionstype)-Element (EAPHost)
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Accept-Servername (Peer-extensionstype)-Element
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- EAPHost-Element
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
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314603"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="0aad6-105">Accept Servername (papextensionstype)-Element (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="0aad6-105">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="0aad6-106">Das Element "Accepted Servername **(Peer-extensionstype)** " gibt an, ob der Servername anhand der im Servername [**(servervalidationparameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegebenen Namens Zeichenfolge validiert wird.</span><span class="sxs-lookup"><span data-stu-id="0aad6-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="0aad6-107">Das-Element wird durch das-Element von " [**Peer**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) Type" definiert.</span><span class="sxs-lookup"><span data-stu-id="0aad6-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aad6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aad6-108">Remarks</span></span>

<span data-ttu-id="0aad6-109">Das Element " **Accept Servername** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="0aad6-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aad6-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aad6-110">Requirements</span></span>



| <span data-ttu-id="0aad6-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aad6-111">Requirement</span></span> | <span data-ttu-id="0aad6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0aad6-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0aad6-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0aad6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0aad6-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aad6-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0aad6-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0aad6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0aad6-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aad6-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0aad6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0aad6-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aad6-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="0aad6-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0aad6-119">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="0aad6-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="0aad6-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="0aad6-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0aad6-121">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="0aad6-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="0aad6-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0aad6-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="0aad6-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="0aad6-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0aad6-124">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="0aad6-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0aad6-125">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="0aad6-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0aad6-126">**Akzeptservername**</span><span class="sxs-lookup"><span data-stu-id="0aad6-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





