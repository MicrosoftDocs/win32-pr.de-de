---
description: Enthält Informationen über eine digitale Signatur.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: SIGNER_SIGNATURE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216203"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="2bbd5-103">Signer \_ Signature \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="2bbd5-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="2bbd5-104">Die Signatur Informationsstruktur der Signatur Geber enthält Informationen über eine digitale Signatur. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="2bbd5-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="2bbd5-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2bbd5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bbd5-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="2bbd5-108">Member</span><span class="sxs-lookup"><span data-stu-id="2bbd5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2bbd5-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="2bbd5-111">**algidhash**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-112">Der für die digitale Signatur verwendete Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="2bbd5-113">**dwattrchoice**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-114">Gibt an, ob die Signatur über [*Authenticode*](../secgloss/a-gly.md) -Attribute verfügt.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="2bbd5-115">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="2bbd5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2bbd5-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="2bbd5-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2bbd5-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="2bbd5-118"><dt>**Signatur \_ Geber AuthCode \_ attr**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2bbd5-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2bbd5-119">Die Signatur verfügt über [*Authenticode*](../secgloss/a-gly.md) -Attribute.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="2bbd5-120"><dt>**Signatur \_ Geber Keine \_ attr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2bbd5-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="2bbd5-121">Die Signatur weist keine [*Authenticode*](../secgloss/a-gly.md) -Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2bbd5-122">**pattrauthcode**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-123">Gibt Attribute für eine [*Authenticode*](../secgloss/a-gly.md) -Signatur an.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="2bbd5-124">Dieser Member ist erforderlich, wenn der Wert des **dwattrchoice** -Members " **Signer \_ AuthCode \_ attr**" lautet.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="2bbd5-125">**psauthenticated**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-126">Von authentifizierten Benutzern angegebene Attribute, die der digitalen Signatur hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="2bbd5-127">**psunauthenticated**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="2bbd5-128">Nicht authentifizierte benutzerdefinierte Attribute, die der digitalen Signatur hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2bbd5-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bbd5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bbd5-129">Requirements</span></span>



| <span data-ttu-id="2bbd5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bbd5-130">Requirement</span></span> | <span data-ttu-id="2bbd5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2bbd5-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bbd5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bbd5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbd5-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bbd5-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2bbd5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bbd5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbd5-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bbd5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bbd5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bbd5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbd5-137">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="2bbd5-138">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="2bbd5-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
