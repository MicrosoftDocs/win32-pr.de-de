---
description: Die "CAPICOM \_ Key Usage"- \_ Enumeration definiert die Methoden, mit denen ein Schlüssel verwendet werden kann. Eingeführt in CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359352"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="aabf5-104">CAPICOM- \_ Schlüssel \_ Verwendungs Enumeration</span><span class="sxs-lookup"><span data-stu-id="aabf5-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="aabf5-105">Die " **CAPICOM \_ Key \_ Usage** "-Enumeration definiert die Methoden, mit denen ein Schlüssel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="aabf5-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="aabf5-106">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="aabf5-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="aabf5-107">Member</span><span class="sxs-lookup"><span data-stu-id="aabf5-107">Members</span></span>



| <span data-ttu-id="aabf5-108">Member</span><span class="sxs-lookup"><span data-stu-id="aabf5-108">Member</span></span>                                      | <span data-ttu-id="aabf5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aabf5-109">Description</span></span>                                                                                                                      | <span data-ttu-id="aabf5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="aabf5-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="aabf5-111">**Verwendung von CAPICOM \_ Digital \_ Signature \_ Key \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="aabf5-112">Der Schlüssel kann verwendet werden, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aabf5-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="aabf5-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="aabf5-113">0x00000080</span></span> |
| <span data-ttu-id="aabf5-114">**Verwendung von CAPICOM- \_ nicht \_ Ablehnungs \_ Schlüsseln \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="aabf5-115">Der Schlüssel kann für die [*Nichtabstreitbarkeit*](../secgloss/n-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="aabf5-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="aabf5-116">0x00000040</span></span> |
| <span data-ttu-id="aabf5-117">**Verwendung des CAPICOM- \_ Schlüssel \_ Verschlüsselungs \_ Schlüssels \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="aabf5-118">Der Schlüssel kann verwendet werden, um einen Schlüssel zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="aabf5-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="aabf5-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="aabf5-119">0x00000020</span></span> |
| <span data-ttu-id="aabf5-120">**Verwendung des CAPICOM- \_ Daten \_ Verschlüsselungs \_ Schlüssels \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="aabf5-121">Der Schlüssel kann zum Verschlüsseln von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="aabf5-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aabf5-122">0x00000010</span></span> |
| <span data-ttu-id="aabf5-123">**Verwendung von CAPICOM \_ Key \_ Agreement \_ Key \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="aabf5-124">Der Schlüssel kann für die Schlüssel Übereinstimmung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="aabf5-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="aabf5-125">0x00000008</span></span> |
| <span data-ttu-id="aabf5-126">**Verwendung von CAPICOM \_ Key \_ CERT \_ Sign \_ Key \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="aabf5-127">Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="aabf5-128">Dieser Wert entspricht der Verwendung von CAPICOM- \_ Offline- \_ CRL- \_ Signatur \_ Schlüsseln \_ .</span><span class="sxs-lookup"><span data-stu-id="aabf5-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="aabf5-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="aabf5-129">0x00000004</span></span> |
| <span data-ttu-id="aabf5-130">**Verwendung von CAPICOM- \_ Offline- \_ CRL- \_ Signatur \_ Schlüsseln \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="aabf5-131">Der Schlüssel kann zum Signieren von Schlüsselzertifikaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="aabf5-132">Dieser Wert entspricht der Verwendung von CAPICOM \_ Key \_ CERT \_ Sign \_ Key \_ .</span><span class="sxs-lookup"><span data-stu-id="aabf5-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="aabf5-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="aabf5-133">0x00000002</span></span> |
| <span data-ttu-id="aabf5-134">**Verwendung von CAPICOM- \_ CRL- \_ Signatur \_ Schlüsseln \_**</span><span class="sxs-lookup"><span data-stu-id="aabf5-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="aabf5-135">Der Schlüssel kann zum Signieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="aabf5-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="aabf5-136">0x00000002</span></span> |
| <span data-ttu-id="aabf5-137">**nur CAPICOM- \_ \_ \_ Schlüssel \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="aabf5-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="aabf5-138">Der Schlüssel kann nur zum Verschlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="aabf5-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aabf5-139">0x00000001</span></span> |
| <span data-ttu-id="aabf5-140">**nur CAPICOM \_ Decipher \_ \_ Key \_ Usage**</span><span class="sxs-lookup"><span data-stu-id="aabf5-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="aabf5-141">Der Schlüssel kann nur zum Entschlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aabf5-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="aabf5-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="aabf5-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="aabf5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aabf5-143">Requirements</span></span>



| <span data-ttu-id="aabf5-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aabf5-144">Requirement</span></span> | <span data-ttu-id="aabf5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="aabf5-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aabf5-146">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="aabf5-146">Redistributable</span></span><br/> | <span data-ttu-id="aabf5-147">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="aabf5-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="aabf5-148">Header</span><span class="sxs-lookup"><span data-stu-id="aabf5-148">Header</span></span><br/>          | <dl> <span data-ttu-id="aabf5-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="aabf5-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
