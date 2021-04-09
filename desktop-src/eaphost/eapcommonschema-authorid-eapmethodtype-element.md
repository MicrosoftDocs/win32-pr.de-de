---
title: Autorisiert (eapmethodtype)-Element
description: Erfahren Sie mehr über das Autorität-Element (eapmethodtype). Das Element "AutorID" (eapmethodtype) verweist auf den Autor der Methode.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- AutorID-Element EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949124"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="02a90-105">Autorisiert (eapmethodtype)-Element</span><span class="sxs-lookup"><span data-stu-id="02a90-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="02a90-106">Das Element " **AutorID" (eapmethodtype)** verweist auf den Autor der Methode.</span><span class="sxs-lookup"><span data-stu-id="02a90-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="02a90-107">Die Autorisierungs-ID ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="02a90-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="02a90-108">Das **Autorität-** Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="02a90-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a90-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02a90-109">Remarks</span></span>

<span data-ttu-id="02a90-110">Die Elemente " **AutorID** " und " [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) " müssen für eine bestimmte Methode nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="02a90-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a90-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02a90-111">Requirements</span></span>



| <span data-ttu-id="02a90-112">Role</span><span class="sxs-lookup"><span data-stu-id="02a90-112">Role</span></span> | <span data-ttu-id="02a90-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="02a90-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="02a90-114">Client</span><span class="sxs-lookup"><span data-stu-id="02a90-114">Client</span></span><br/> | <span data-ttu-id="02a90-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02a90-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02a90-116">Server</span><span class="sxs-lookup"><span data-stu-id="02a90-116">Server</span></span><br/> | <span data-ttu-id="02a90-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02a90-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02a90-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02a90-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="02a90-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="02a90-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="02a90-120">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="02a90-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="02a90-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="02a90-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="02a90-122">eapcommon-Schema</span><span class="sxs-lookup"><span data-stu-id="02a90-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





