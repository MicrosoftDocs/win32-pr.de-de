---
title: Type (eapmethodtype)-Element
description: Erfahren Sie mehr über das Type (eapmethodtype)-Element, das auf den EAP-Methodentyp verweist. Informationen finden Sie unter Anforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Type-Element EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391017"
---
# <a name="type-eapmethodtype-element"></a><span data-ttu-id="d9665-105">Type (eapmethodtype)-Element</span><span class="sxs-lookup"><span data-stu-id="d9665-105">Type (EapMethodType) Element</span></span>

<span data-ttu-id="d9665-106">Das **Type (eapmethodtype)** -Element verweist auf den EAP-Methodentyp.</span><span class="sxs-lookup"><span data-stu-id="d9665-106">The **Type (EapMethodType)** element refers to the EAP method type.</span></span>

<span data-ttu-id="d9665-107">Der Typ ist eine eindeutige Zahl, die von der Internet Assigned Numbers Authority (IANA) ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9665-107">The Type is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

<span data-ttu-id="d9665-108">Das **Type** -Element wird durch den komplexen [**eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="d9665-108">The **Type** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9665-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9665-109">Requirements</span></span>



| <span data-ttu-id="d9665-110">Role</span><span class="sxs-lookup"><span data-stu-id="d9665-110">Role</span></span> | <span data-ttu-id="d9665-111">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="d9665-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d9665-112">Client</span><span class="sxs-lookup"><span data-stu-id="d9665-112">Client</span></span><br/> | <span data-ttu-id="d9665-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9665-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9665-114">Server</span><span class="sxs-lookup"><span data-stu-id="d9665-114">Server</span></span><br/> | <span data-ttu-id="d9665-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9665-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9665-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9665-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9665-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d9665-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9665-118">**Eapmethodtype**</span><span class="sxs-lookup"><span data-stu-id="d9665-118">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="d9665-119">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="d9665-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d9665-120">eapcommon-Schema</span><span class="sxs-lookup"><span data-stu-id="d9665-120">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





