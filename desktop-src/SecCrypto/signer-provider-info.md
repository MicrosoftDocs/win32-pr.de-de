---
description: Gibt die Informationen zum Kryptografiedienstanbieter (CSP) und zum privaten Schlüssel an, die zum Erstellen einer digitalen Signatur verwendet werden.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364134"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="e2037-103">\_Informationsstruktur des Signatur Geber Anbieters \_</span><span class="sxs-lookup"><span data-stu-id="e2037-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="e2037-104">Die Informationen Struktur des **Signatur \_ Geber Anbieters \_** gibt die Informationen zum [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und zum privaten Schlüssel an, die zum Erstellen einer digitalen Signatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2037-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="e2037-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="e2037-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="e2037-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e2037-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e2037-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2037-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="e2037-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2037-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2037-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="e2037-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e2037-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2037-111">**pwszprovidername**</span><span class="sxs-lookup"><span data-stu-id="e2037-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-112">Der Name des CSP, der zum Erstellen der digitalen Signatur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2037-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="e2037-113">Wenn der Wert dieses Members **null** ist, wird der Standardanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2037-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="e2037-114">**dwprovidertype**</span><span class="sxs-lookup"><span data-stu-id="e2037-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-115">Der vom **pwszprovidername** -Member angegebene Typ des CSP.</span><span class="sxs-lookup"><span data-stu-id="e2037-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="e2037-116">**dwkeyspec**</span><span class="sxs-lookup"><span data-stu-id="e2037-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-117">Die Schlüsselspezifikation.</span><span class="sxs-lookup"><span data-stu-id="e2037-117">The key specification.</span></span> <span data-ttu-id="e2037-118">Wenn dieses Element auf 0 (null) festgelegt ist, wird die Schlüssel Spezifikation im Member **pwszpvkfilename** oder **pwszkeycontainer** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2037-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="e2037-119">Wenn im **pwszkeycontainer** -Member mehr als eine Schlüssel Spezifikation vorhanden ist, wird **bei der \_ Signatur** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2037-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="e2037-120">Wenn dies nicht möglich ist, wird **bei \_ keyexchange** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2037-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="e2037-121">**dwpvkchoice**</span><span class="sxs-lookup"><span data-stu-id="e2037-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-122">Gibt den Typ der Informationen zum privaten Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="e2037-122">Specifies the type of private key information.</span></span> <span data-ttu-id="e2037-123">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e2037-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="e2037-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e2037-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="e2037-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2037-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="e2037-126"><dt>**PVK \_ \_ \_ Dateiname**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e2037-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="e2037-127">Die Informationen zum privaten Schlüssel sind ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="e2037-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="e2037-128"><dt>**PVK \_ Geben Sie \_ keycontainer**</dt> <dt>2 (0x2)</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="e2037-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="e2037-129">Die Informationen zum privaten Schlüssel sind ein Schlüssel Container.</span><span class="sxs-lookup"><span data-stu-id="e2037-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2037-130">**pwszpvkfilename**</span><span class="sxs-lookup"><span data-stu-id="e2037-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-131">Der Name der Datei, die die Informationen zum privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="e2037-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="e2037-132">**pwszkeycontainer**</span><span class="sxs-lookup"><span data-stu-id="e2037-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="e2037-133">Der Name des Schlüssel Containers, der die Informationen zum privaten Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="e2037-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2037-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2037-134">Requirements</span></span>



| <span data-ttu-id="e2037-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2037-135">Requirement</span></span> | <span data-ttu-id="e2037-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e2037-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2037-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2037-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e2037-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2037-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e2037-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2037-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e2037-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2037-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2037-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2037-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2037-142">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="e2037-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="e2037-143">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="e2037-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
