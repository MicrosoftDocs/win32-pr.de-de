---
title: Akzeptservername
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Akzeptservername
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219264"
---
# <a name="acceptservername"></a><span data-ttu-id="4aa0e-105">Akzeptservername</span><span class="sxs-lookup"><span data-stu-id="4aa0e-105">AcceptServerName</span></span>

<span data-ttu-id="4aa0e-106">Das Element "Accept Servername **(eaptype)** " gibt an, ob der Servername anhand der namens Zeichenfolge überprüft wird, die im Servername [**(servervalidationparameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="4aa0e-107">Das-Element wird durch das [**eaptype**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa0e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aa0e-108">Remarks</span></span>

<span data-ttu-id="4aa0e-109">Das Element " **Accept Servername** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="4aa0e-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa0e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aa0e-110">Requirements</span></span>



| <span data-ttu-id="4aa0e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aa0e-111">Requirement</span></span> | <span data-ttu-id="4aa0e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4aa0e-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4aa0e-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aa0e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa0e-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aa0e-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4aa0e-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aa0e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa0e-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aa0e-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4aa0e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aa0e-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aa0e-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4aa0e-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa0e-119">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4aa0e-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="4aa0e-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4aa0e-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa0e-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4aa0e-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="4aa0e-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4aa0e-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4aa0e-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="4aa0e-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4aa0e-124">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="4aa0e-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4aa0e-125">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="4aa0e-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4aa0e-126">**"Accept Servername" (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="4aa0e-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





