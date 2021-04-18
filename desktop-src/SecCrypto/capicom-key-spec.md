---
description: Die CAPICOM \_ Key \_ spec-Enumeration definiert Schlüssel Spezifikationen.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: CAPICOM_KEY_SPEC-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364685"
---
# <a name="capicom_key_spec-enumeration"></a><span data-ttu-id="6ce09-103">CAPICOM- \_ schlüsselspezifikations \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="6ce09-103">CAPICOM\_KEY\_SPEC enumeration</span></span>

<span data-ttu-id="6ce09-104">Die **CAPICOM \_ Key \_ spec** -Enumeration definiert Schlüssel Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6ce09-104">The **CAPICOM\_KEY\_SPEC** enumeration defines key specifications.</span></span>

## <a name="members"></a><span data-ttu-id="6ce09-105">Member</span><span class="sxs-lookup"><span data-stu-id="6ce09-105">Members</span></span>



| <span data-ttu-id="6ce09-106">Member</span><span class="sxs-lookup"><span data-stu-id="6ce09-106">Member</span></span>                              | <span data-ttu-id="6ce09-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ce09-107">Description</span></span>                                                | <span data-ttu-id="6ce09-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6ce09-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|-------|
| <span data-ttu-id="6ce09-109">**CAPICOM- \_ Schlüssel \_ Spezifikation \_ keyexchange**</span><span class="sxs-lookup"><span data-stu-id="6ce09-109">**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</span></span> | <span data-ttu-id="6ce09-110">Der Schlüssel kann für die Verschlüsselung und Signierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ce09-110">The key can be used for encryption and signing.</span></span><br/> | <span data-ttu-id="6ce09-111">1</span><span class="sxs-lookup"><span data-stu-id="6ce09-111">1</span></span>     |
| <span data-ttu-id="6ce09-112">**CAPICOM \_ Key \_ spec- \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="6ce09-112">**CAPICOM\_KEY\_SPEC\_SIGNATURE**</span></span>   | <span data-ttu-id="6ce09-113">Der Schlüssel kann nur für die Signierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ce09-113">The key can be used only for signing.</span></span><br/>           | <span data-ttu-id="6ce09-114">2</span><span class="sxs-lookup"><span data-stu-id="6ce09-114">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="6ce09-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ce09-115">Remarks</span></span>

<span data-ttu-id="6ce09-116">Die **CAPICOM \_ - \_ schlüsselspezifikations** Enumeration wird von den folgenden Methoden und Eigenschaften verwendet:</span><span class="sxs-lookup"><span data-stu-id="6ce09-116">The **CAPICOM\_KEY\_SPEC** enumeration is used by the following methods and properties:</span></span>

-   <span data-ttu-id="6ce09-117">[**PrivateKey. KeySpec**](privatekey-keyspec.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ce09-117">[**PrivateKey.KeySpec**](privatekey-keyspec.md) property.</span></span>
-   <span data-ttu-id="6ce09-118">[**PrivateKey. Open**](privatekey-open.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6ce09-118">[**PrivateKey.Open**](privatekey-open.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce09-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ce09-119">Requirements</span></span>



| <span data-ttu-id="6ce09-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ce09-120">Requirement</span></span> | <span data-ttu-id="6ce09-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6ce09-121">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce09-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6ce09-122">Redistributable</span></span><br/> | <span data-ttu-id="6ce09-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ce09-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="6ce09-124">Header</span><span class="sxs-lookup"><span data-stu-id="6ce09-124">Header</span></span><br/>          | <dl> <span data-ttu-id="6ce09-125"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ce09-125"><dt>Capicom.h</dt></span></span> </dl> |



 

 




