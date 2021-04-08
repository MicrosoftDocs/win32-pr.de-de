---
title: Usewinlogonanmeldeinformationen (eaptype)-Element
description: Erfahren Sie mehr über das usewinlogonanmelde-Element (eaptype)-Element. Dieses Element steuert die Verwendung von winlogin-Anmelde Informationen.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Usewinlogon-Anmelde Informationen-Element EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730369"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="88b2c-105">Usewinlogonanmeldeinformationen (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="88b2c-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="88b2c-106">Das **usewinlogonanmeldeinformationen (eaptype)** -Element steuert die Verwendung der winlogin-Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="88b2c-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="88b2c-107">Das **usewinlogonanmelde** -Element wird durch das [**eaptype**](mschapv2connectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="88b2c-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b2c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88b2c-108">Remarks</span></span>

<span data-ttu-id="88b2c-109">Wenn der Wert true ist, erhält der EAP-MS-CHAPv2 Anmelde Informationen von Winlogon.</span><span class="sxs-lookup"><span data-stu-id="88b2c-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="88b2c-110">Wenn der Wert false ist, erhält EAP MS-CHAPv2 Anmelde Informationen vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="88b2c-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="88b2c-111">Das **usewinlogon-Anmelde Informationen-Element (eaptype)** ist optional.</span><span class="sxs-lookup"><span data-stu-id="88b2c-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b2c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88b2c-112">Requirements</span></span>



| <span data-ttu-id="88b2c-113">Role</span><span class="sxs-lookup"><span data-stu-id="88b2c-113">Role</span></span> | <span data-ttu-id="88b2c-114">Mindestens unterstützte Betriebssystemversionen</span><span class="sxs-lookup"><span data-stu-id="88b2c-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="88b2c-115">Client</span><span class="sxs-lookup"><span data-stu-id="88b2c-115">Client</span></span><br/> | <span data-ttu-id="88b2c-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88b2c-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88b2c-117">Server</span><span class="sxs-lookup"><span data-stu-id="88b2c-117">Server</span></span><br/> | <span data-ttu-id="88b2c-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88b2c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88b2c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88b2c-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="88b2c-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="88b2c-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="88b2c-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="88b2c-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="88b2c-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="88b2c-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="88b2c-123">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="88b2c-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="88b2c-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="88b2c-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="88b2c-125">mschapv2connectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="88b2c-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





