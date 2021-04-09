---
title: Username-Element (CHAP)
description: Erfahren Sie mehr über das UserName-Element, das den Benutzer identifiziert, der authentifiziert wird. Weitere Informationen finden Sie in einem Syntax Beispiel.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
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
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949115"
---
# <a name="username-element-chap"></a><span data-ttu-id="2cd71-105">Username-Element (CHAP)</span><span class="sxs-lookup"><span data-stu-id="2cd71-105">Username element (CHAP)</span></span>

<span data-ttu-id="2cd71-106">Das **username** -Element identifiziert den Benutzer, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2cd71-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="2cd71-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cd71-107">Remarks</span></span>

<span data-ttu-id="2cd71-108">Wenn das **username** -Element nicht vorhanden ist, wird der Benutzername aus Winlogon abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2cd71-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="2cd71-109">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="2cd71-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd71-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cd71-110">Requirements</span></span>



| <span data-ttu-id="2cd71-111">Role</span><span class="sxs-lookup"><span data-stu-id="2cd71-111">Role</span></span> | <span data-ttu-id="2cd71-112">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="2cd71-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2cd71-113">Client</span><span class="sxs-lookup"><span data-stu-id="2cd71-113">Client</span></span><br/> | <span data-ttu-id="2cd71-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd71-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2cd71-115">Server</span><span class="sxs-lookup"><span data-stu-id="2cd71-115">Server</span></span><br/> | <span data-ttu-id="2cd71-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cd71-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cd71-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cd71-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd71-118">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="2cd71-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2cd71-119">mschapv2userpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="2cd71-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





