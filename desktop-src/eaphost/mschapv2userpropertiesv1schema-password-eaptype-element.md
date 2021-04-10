---
title: Password (eaptype)-Element
description: Erfahren Sie mehr über das Password (eaptype)-Element. Dieses Element identifiziert das Kennwort für den Benutzer oder Computer, der authentifiziert wird.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Password-Element EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039624"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="4b7aa-105">Password (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="4b7aa-105">Password (EapType) Element</span></span>

<span data-ttu-id="4b7aa-106">Das **Kennwort-Element (eaptype)** identifiziert das Kennwort des Benutzers oder Computers, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="4b7aa-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="4b7aa-107">Das **Password** -Element wird durch das [**eaptype**](mschapv2userpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4b7aa-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b7aa-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b7aa-108">Remarks</span></span>

<span data-ttu-id="4b7aa-109">Wenn das **Password-Element (eaptype)** nicht vorhanden ist, wird der Kenn Wort Hash von Winlogon abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b7aa-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="4b7aa-110">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b7aa-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7aa-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b7aa-111">Requirements</span></span>



| <span data-ttu-id="4b7aa-112">Role</span><span class="sxs-lookup"><span data-stu-id="4b7aa-112">Role</span></span> | <span data-ttu-id="4b7aa-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="4b7aa-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="4b7aa-114">Client</span><span class="sxs-lookup"><span data-stu-id="4b7aa-114">Client</span></span><br/> | <span data-ttu-id="4b7aa-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b7aa-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b7aa-116">Server</span><span class="sxs-lookup"><span data-stu-id="4b7aa-116">Server</span></span><br/> | <span data-ttu-id="4b7aa-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b7aa-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b7aa-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b7aa-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b7aa-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4b7aa-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4b7aa-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4b7aa-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="4b7aa-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4b7aa-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4b7aa-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4b7aa-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="4b7aa-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="4b7aa-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4b7aa-124">mschapv2userpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="4b7aa-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





