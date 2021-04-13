---
title: VendorID (eapmethodtype)-Element
description: Bezieht sich auf den Hersteller, der die-Methode definiert hat, wenn das Type (eapmethodtype)-Element 254 (eine erweiterte EAP-Methode) ist.
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- VendorID-Element EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517891"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="f237d-104">VendorID (eapmethodtype)-Element</span><span class="sxs-lookup"><span data-stu-id="f237d-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="f237d-105">Das **VendorID (eapmethodtype)-** Element verweist auf den Hersteller, der die Methode definiert hat, wenn das [**Type (eapmethodtype)**](eapcommonschema-type-eapmethodtype-element.md) -Element 254 (eine erweiterte EAP-Methode) ist.</span><span class="sxs-lookup"><span data-stu-id="f237d-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="f237d-106">**VendorID** ist optional.</span><span class="sxs-lookup"><span data-stu-id="f237d-106">The **VendorId** is optional.</span></span> <span data-ttu-id="f237d-107">Bei Verwendung ist **VendorID** eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f237d-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="f237d-108">Das **VendorID-** Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f237d-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f237d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f237d-109">Remarks</span></span>

<span data-ttu-id="f237d-110">Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md) " und " **VendorID** " müssen für eine bestimmte Methode nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f237d-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f237d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f237d-111">Requirements</span></span>



| <span data-ttu-id="f237d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f237d-112">Requirement</span></span> | <span data-ttu-id="f237d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f237d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f237d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f237d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f237d-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f237d-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f237d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f237d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f237d-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f237d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f237d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f237d-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f237d-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="f237d-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f237d-120">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="f237d-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="f237d-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="f237d-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f237d-122">eapcommon-Schema</span><span class="sxs-lookup"><span data-stu-id="f237d-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





