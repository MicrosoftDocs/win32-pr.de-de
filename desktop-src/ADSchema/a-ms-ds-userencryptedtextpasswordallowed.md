---
title: ms-DS-User-verschlüsselte-Text-Password-Allowed-Attribut
description: Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungs Format speichert.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-verschlüsselte-Text-Password-Allowed\"-Attribut AD-Schema"
- AD-Schema für das Attribut "ms-DS-userencryptedtextpasswordallowed"
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479759"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="68ec8-105">ms-DS-User-verschlüsselte-Text-Password-Allowed-Attribut</span><span class="sxs-lookup"><span data-stu-id="68ec8-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="68ec8-106">Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungs Format speichert.</span><span class="sxs-lookup"><span data-stu-id="68ec8-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="68ec8-107">True, wenn das Kennwort im umkehrbaren Verschlüsselungs Format gespeichert ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="68ec8-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="68ec8-108">Dieses Attribut wird nicht von [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) verwendet und ist nur aus Gründen der Vollständigkeit/Parität mit userAccountControl enthalten.</span><span class="sxs-lookup"><span data-stu-id="68ec8-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="68ec8-109">AD LDS speichert keine Kenn Wörter mit umkehrbarer Verschlüsselung, unabhängig vom Wert dieses Attributs für ein bestimmtes Objekt oder die Sicherheitsrichtlinie des Computers in Bezug auf die umkehrbare Verschlüsselung auf dem Computer selbst.</span><span class="sxs-lookup"><span data-stu-id="68ec8-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="68ec8-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="68ec8-110">Entry</span></span> | <span data-ttu-id="68ec8-111">Wert</span><span class="sxs-lookup"><span data-stu-id="68ec8-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="68ec8-112">CN</span><span class="sxs-lookup"><span data-stu-id="68ec8-112">CN</span></span>                | <span data-ttu-id="68ec8-113">ms-DS-Benutzer-verschlüsselt-Text-Kennwort zulässig</span><span class="sxs-lookup"><span data-stu-id="68ec8-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="68ec8-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="68ec8-114">Ldap-Display-Name</span></span> | <span data-ttu-id="68ec8-115">ms-DS-userencryptedtextpasswordallowed</span><span class="sxs-lookup"><span data-stu-id="68ec8-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="68ec8-116">Size</span><span class="sxs-lookup"><span data-stu-id="68ec8-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="68ec8-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="68ec8-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="68ec8-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="68ec8-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="68ec8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="68ec8-119">Attribute-Id</span></span>      | <span data-ttu-id="68ec8-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="68ec8-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="68ec8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="68ec8-121">System-Id-Guid</span></span>    | <span data-ttu-id="68ec8-122">5a87c7f 2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="68ec8-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="68ec8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ec8-123">Syntax</span></span>            | [<span data-ttu-id="68ec8-124">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="68ec8-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="68ec8-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="68ec8-125">Implementations</span></span>

-   [<span data-ttu-id="68ec8-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="68ec8-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="68ec8-127">Adam</span><span class="sxs-lookup"><span data-stu-id="68ec8-127">ADAM</span></span>



| <span data-ttu-id="68ec8-128">Eingabe</span><span class="sxs-lookup"><span data-stu-id="68ec8-128">Entry</span></span> | <span data-ttu-id="68ec8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="68ec8-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="68ec8-130">Link-ID</span><span class="sxs-lookup"><span data-stu-id="68ec8-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="68ec8-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="68ec8-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="68ec8-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="68ec8-132">System-Only</span></span>            | <span data-ttu-id="68ec8-133">False</span><span class="sxs-lookup"><span data-stu-id="68ec8-133">False</span></span>                                                             |
| <span data-ttu-id="68ec8-134">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="68ec8-134">Is-Single-Valued</span></span>       | <span data-ttu-id="68ec8-135">Richtig</span><span class="sxs-lookup"><span data-stu-id="68ec8-135">True</span></span>                                                              |
| <span data-ttu-id="68ec8-136">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="68ec8-136">Is Indexed</span></span>             | <span data-ttu-id="68ec8-137">False</span><span class="sxs-lookup"><span data-stu-id="68ec8-137">False</span></span>                                                             |
| <span data-ttu-id="68ec8-138">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="68ec8-138">In Global Catalog</span></span>      | <span data-ttu-id="68ec8-139">False</span><span class="sxs-lookup"><span data-stu-id="68ec8-139">False</span></span>                                                             |
| <span data-ttu-id="68ec8-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="68ec8-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="68ec8-141">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="68ec8-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="68ec8-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="68ec8-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="68ec8-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="68ec8-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="68ec8-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="68ec8-144">Search-Flags</span></span>           | <span data-ttu-id="68ec8-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="68ec8-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="68ec8-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="68ec8-146">System-Flags</span></span>           | <span data-ttu-id="68ec8-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68ec8-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="68ec8-148">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="68ec8-148">Classes used in</span></span>        | [<span data-ttu-id="68ec8-149">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="68ec8-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="68ec8-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68ec8-150">Remarks</span></span>

<span data-ttu-id="68ec8-151">In Adam ersetzt dieses Attribut das Flag " [**ADS- \_ \_ verschlüsseltes \_ \_ textkennwort \_ zulässig**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " des Attributs " [**userAccountControl**](a-useraccountcontrol.md) ".</span><span class="sxs-lookup"><span data-stu-id="68ec8-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

