---
title: Komplexer eapmethodtype-Typ
description: Definiert die Elemente, die einen einzelnen EAP-Methodentyp, VendorID, vendortype und AutorID eindeutig identifizieren.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Komplexer EAP-Typ eapmethodtype EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741841"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="1318f-104">Komplexer eapmethodtype-Typ</span><span class="sxs-lookup"><span data-stu-id="1318f-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="1318f-105">Der komplexe Typ **eapmethodtype** definiert die Elemente, die eine einzelne EAP-Methode eindeutig identifizieren: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md)und [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="1318f-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="1318f-106">[**Typ**](eapcommonschema-type-eapmethodtype-element.md) und [**Autorität**](eapcommonschema-authorid-eapmethodtype-element.md) sind obligatorische Elemente, während [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) und [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) nur erforderlich sind, wenn das **Type** -Element 254 (eine erweiterte EAP-Methode) ist.</span><span class="sxs-lookup"><span data-stu-id="1318f-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1318f-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1318f-107">Child elements</span></span>



| <span data-ttu-id="1318f-108">Element</span><span class="sxs-lookup"><span data-stu-id="1318f-108">Element</span></span>                                                                | <span data-ttu-id="1318f-109">type</span><span class="sxs-lookup"><span data-stu-id="1318f-109">Type</span></span>         | <span data-ttu-id="1318f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1318f-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1318f-111">**AutorID**</span><span class="sxs-lookup"><span data-stu-id="1318f-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="1318f-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1318f-112">unsignedInt</span></span>  | <span data-ttu-id="1318f-113">Verweist auf den Autor der Methode.</span><span class="sxs-lookup"><span data-stu-id="1318f-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="1318f-114">**type**</span><span class="sxs-lookup"><span data-stu-id="1318f-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="1318f-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1318f-115">unsignedByte</span></span> | <span data-ttu-id="1318f-116">Bezieht sich auf den Typ der EAP-Methode.</span><span class="sxs-lookup"><span data-stu-id="1318f-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="1318f-117">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="1318f-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="1318f-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1318f-118">unsignedInt</span></span>  | <span data-ttu-id="1318f-119">Verweist auf den Hersteller, der die-Methode definiert hat,, wenn das [**Type**](eapcommonschema-type-eapmethodtype-element.md) -Element 254 (eine erweiterte EAP-Methode) ist.</span><span class="sxs-lookup"><span data-stu-id="1318f-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="1318f-120">[**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) ist optional.</span><span class="sxs-lookup"><span data-stu-id="1318f-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="1318f-121">**Vendortype**</span><span class="sxs-lookup"><span data-stu-id="1318f-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="1318f-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1318f-122">unsignedInt</span></span>  | <span data-ttu-id="1318f-123">Ist der Hersteller definierte Typ für die Methode.</span><span class="sxs-lookup"><span data-stu-id="1318f-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="1318f-124">Der [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) ist optional.</span><span class="sxs-lookup"><span data-stu-id="1318f-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="1318f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1318f-125">Remarks</span></span>

<span data-ttu-id="1318f-126">Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md) " und " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " müssen für eine bestimmte Methode nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1318f-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="1318f-127">Die Elemente " [**AutorID**](eapcommonschema-authorid-eapmethodtype-element.md)", " [**Type**](eapcommonschema-type-eapmethodtype-element.md)", " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " und " [**vendortype**](eapcommonschema-vendortype-eapmethodtype-element.md) " sind jeweils eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1318f-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="1318f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1318f-128">Requirements</span></span>



| <span data-ttu-id="1318f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1318f-129">Requirement</span></span> | <span data-ttu-id="1318f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1318f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1318f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1318f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1318f-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1318f-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1318f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1318f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1318f-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1318f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1318f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1318f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1318f-136">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="1318f-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1318f-137">eapcommon-Schema</span><span class="sxs-lookup"><span data-stu-id="1318f-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





