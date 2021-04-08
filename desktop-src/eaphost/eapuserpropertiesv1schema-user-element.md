---
title: User-Element
description: Erfahren Sie mehr über das User-Element. Dieses Element wird nicht verwendet, wenn Legacy Methoden über die EAPHost-APIs verwendet werden.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- User-Element EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730361"
---
# <a name="user-element"></a><span data-ttu-id="5a965-105">User-Element</span><span class="sxs-lookup"><span data-stu-id="5a965-105">User Element</span></span>

<span data-ttu-id="5a965-106">Das **User** -Element wird nicht verwendet, wenn Legacy Methoden über die EAPHost-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a965-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="5a965-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a965-107">Child elements</span></span>



| <span data-ttu-id="5a965-108">Element</span><span class="sxs-lookup"><span data-stu-id="5a965-108">Element</span></span>                                                  | <span data-ttu-id="5a965-109">type</span><span class="sxs-lookup"><span data-stu-id="5a965-109">Type</span></span> | <span data-ttu-id="5a965-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a965-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="5a965-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="5a965-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="5a965-112">Zeichnet den Methodentyp und die Methoden spezifischen Anmelde Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="5a965-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a965-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a965-113">Requirements</span></span>



| <span data-ttu-id="5a965-114">Role</span><span class="sxs-lookup"><span data-stu-id="5a965-114">Role</span></span> | <span data-ttu-id="5a965-115">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="5a965-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="5a965-116">Client</span><span class="sxs-lookup"><span data-stu-id="5a965-116">Client</span></span><br/> | <span data-ttu-id="5a965-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a965-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a965-118">Server</span><span class="sxs-lookup"><span data-stu-id="5a965-118">Server</span></span><br/> | <span data-ttu-id="5a965-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a965-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a965-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a965-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a965-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="5a965-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5a965-122">eapuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="5a965-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





