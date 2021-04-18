---
title: Username-Element (TLS)
description: Erfahren Sie mehr über das UserName-Element. Dieses Element erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Username-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340736"
---
# <a name="username-element-tls"></a><span data-ttu-id="1446d-105">Username-Element (TLS)</span><span class="sxs-lookup"><span data-stu-id="1446d-105">Username element (TLS)</span></span>

<span data-ttu-id="1446d-106">Das **username** -Element erfasst den Benutzernamen, der in der EAP-Identity-Antwort gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1446d-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="1446d-107">Wenn das **username** -Element nicht vorhanden ist, verwendet EAP-TLS den Namen in dem Zertifikat, auf das im [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1446d-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="1446d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1446d-108">Requirements</span></span>



| <span data-ttu-id="1446d-109">Role</span><span class="sxs-lookup"><span data-stu-id="1446d-109">Role</span></span> | <span data-ttu-id="1446d-110">Mindestens unterstützte Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="1446d-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="1446d-111">Client</span><span class="sxs-lookup"><span data-stu-id="1446d-111">Client</span></span><br/> | <span data-ttu-id="1446d-112">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1446d-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1446d-113">Server</span><span class="sxs-lookup"><span data-stu-id="1446d-113">Server</span></span><br/> | <span data-ttu-id="1446d-114">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1446d-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1446d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1446d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1446d-116">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="1446d-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1446d-117">eaptlsuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="1446d-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





