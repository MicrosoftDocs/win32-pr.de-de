---
title: UserCert-Element (eaptype)
description: Bezieht sich auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- UserCert-Element EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743200"
---
# <a name="usercert-eaptype-element"></a><span data-ttu-id="97ea7-104">UserCert-Element (eaptype)</span><span class="sxs-lookup"><span data-stu-id="97ea7-104">UserCert (EapType) Element</span></span>

<span data-ttu-id="97ea7-105">Das **userCert-Element (eaptype)** verweist auf den SHA-1-Hash des Zertifikats, das für die Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97ea7-105">The **UserCert (EapType)** element refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span>

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

<span data-ttu-id="97ea7-106">Das **userCert** -Element wird durch das [**eaptype**](eaptlsuserpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="97ea7-106">The **UserCert** element is defined by the [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ea7-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97ea7-107">Requirements</span></span>



| <span data-ttu-id="97ea7-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97ea7-108">Requirement</span></span> | <span data-ttu-id="97ea7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="97ea7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97ea7-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97ea7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="97ea7-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97ea7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97ea7-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97ea7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="97ea7-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97ea7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97ea7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97ea7-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="97ea7-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="97ea7-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="97ea7-116">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="97ea7-116">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="97ea7-117">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="97ea7-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="97ea7-118">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="97ea7-118">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="97ea7-119">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="97ea7-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="97ea7-120">eaptlsuserpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="97ea7-120">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





