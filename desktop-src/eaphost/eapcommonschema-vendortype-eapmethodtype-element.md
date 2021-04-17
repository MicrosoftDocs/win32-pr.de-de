---
title: Vendortype (eapmethodtype)-Element
description: Erfahren Sie mehr über das vendortype (eapmethodtype)-Element. Dieses Element ist der Hersteller definierte Typ für die-Methode.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Vendortype-Element EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474220"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="63b63-105">Vendortype (eapmethodtype)-Element</span><span class="sxs-lookup"><span data-stu-id="63b63-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="63b63-106">Das **vendortype (eapmethodtype)** -Element ist der Hersteller definierte Typ für die-Methode.</span><span class="sxs-lookup"><span data-stu-id="63b63-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="63b63-107">Das **vendortype** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63b63-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="63b63-108">Bei Verwendung ist **vendortype** eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="63b63-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="63b63-109">Das **vendortype** -Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="63b63-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b63-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63b63-110">Requirements</span></span>



| <span data-ttu-id="63b63-111">Role</span><span class="sxs-lookup"><span data-stu-id="63b63-111">Role</span></span> | <span data-ttu-id="63b63-112">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="63b63-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="63b63-113">Client</span><span class="sxs-lookup"><span data-stu-id="63b63-113">Client</span></span><br/> | <span data-ttu-id="63b63-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63b63-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63b63-115">Server</span><span class="sxs-lookup"><span data-stu-id="63b63-115">Server</span></span><br/> | <span data-ttu-id="63b63-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63b63-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63b63-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63b63-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="63b63-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="63b63-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="63b63-119">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="63b63-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="63b63-120">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="63b63-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="63b63-121">eapcommon-Schema</span><span class="sxs-lookup"><span data-stu-id="63b63-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





