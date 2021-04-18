---
title: Accepted Servername-Element
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Accepted Servername-Element
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Accept-Servername-Element EAPHost
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351876"
---
# <a name="acceptservername-element"></a><span data-ttu-id="e00df-105">Accepted Servername-Element</span><span class="sxs-lookup"><span data-stu-id="e00df-105">AcceptServerName element</span></span>

<span data-ttu-id="e00df-106">Das Element "Accept Servername **(eaptype)** " gibt an, ob der Servername anhand der namens Zeichenfolge überprüft wird, die im Servername [**(servervalidationparameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e00df-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="e00df-107">Das Element " **Accept Servername** " wird durch das [**eaptype**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="e00df-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00df-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e00df-108">Remarks</span></span>

<span data-ttu-id="e00df-109">Das Element " **Accept Servername** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="e00df-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00df-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e00df-110">Requirements</span></span>



| <span data-ttu-id="e00df-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e00df-111">Requirement</span></span> | <span data-ttu-id="e00df-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e00df-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e00df-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e00df-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e00df-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e00df-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e00df-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e00df-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e00df-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e00df-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e00df-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e00df-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e00df-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="e00df-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e00df-119">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="e00df-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e00df-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="e00df-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e00df-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="e00df-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e00df-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e00df-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e00df-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="e00df-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e00df-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="e00df-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e00df-125">eaptlsconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="e00df-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e00df-126">**"Accept Servername" (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="e00df-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





