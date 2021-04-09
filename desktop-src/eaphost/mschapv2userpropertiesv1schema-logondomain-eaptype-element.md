---
title: LogonDomain (eaptype)-Element
description: Erfahren Sie mehr über das LogonDomain (eaptype)-Element. Dieses Element identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- LogonDomain-Element EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039594"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="63ce5-105">LogonDomain (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="63ce5-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="63ce5-106">Das **LogonDomain (eaptype)** -Element identifiziert die Domäne des Benutzers oder Computers, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="63ce5-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="63ce5-107">Das **LogonDomain** -Element wird durch das [**eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="63ce5-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="63ce5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63ce5-108">Remarks</span></span>

<span data-ttu-id="63ce5-109">Wenn das **LogonDomain (eaptype)** -Element nicht vorhanden ist, wird die Domäne von Winlogon verwendet.</span><span class="sxs-lookup"><span data-stu-id="63ce5-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="63ce5-110">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="63ce5-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ce5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63ce5-111">Requirements</span></span>



| <span data-ttu-id="63ce5-112">Role</span><span class="sxs-lookup"><span data-stu-id="63ce5-112">Role</span></span> | <span data-ttu-id="63ce5-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="63ce5-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="63ce5-114">Client</span><span class="sxs-lookup"><span data-stu-id="63ce5-114">Client</span></span><br/> | <span data-ttu-id="63ce5-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63ce5-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63ce5-116">Server</span><span class="sxs-lookup"><span data-stu-id="63ce5-116">Server</span></span><br/> | <span data-ttu-id="63ce5-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63ce5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63ce5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63ce5-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="63ce5-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="63ce5-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="63ce5-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="63ce5-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="63ce5-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="63ce5-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="63ce5-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="63ce5-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="63ce5-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="63ce5-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="63ce5-124">mschapv2userpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="63ce5-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





