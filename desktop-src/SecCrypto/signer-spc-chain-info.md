---
description: Gibt ein Software Herausgeber Zertifikat (SPC) und eine Zertifikat Kette zum Signieren eines Dokuments an.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131649"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="3641c-103">Info Struktur der Signatur Geber- \_ SPC- \_ Kette \_</span><span class="sxs-lookup"><span data-stu-id="3641c-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="3641c-104">Die Informationen Struktur der Signatur Geber- **\_ SPC- \_ Kette \_** gibt ein [*Software Herausgeber Zertifikat*](../secgloss/s-gly.md) (SPC) und eine Zertifikat Kette zum Signieren eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="3641c-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="3641c-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="3641c-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="3641c-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3641c-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3641c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3641c-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="3641c-108">Member</span><span class="sxs-lookup"><span data-stu-id="3641c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3641c-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="3641c-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3641c-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3641c-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="3641c-111">**pwszspcfile**</span><span class="sxs-lookup"><span data-stu-id="3641c-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="3641c-112">Der Name der SPC-Datei, die zum Signieren eines Dokuments verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3641c-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="3641c-113">**dwcertpolicy**</span><span class="sxs-lookup"><span data-stu-id="3641c-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="3641c-114">Gibt an, wie der Signatur Zertifikate hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3641c-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="3641c-115">Zum Ermitteln der Zertifikat Kette werden die Speicher "My", "ca", "root" und "SPC" zusätzlich zu dem vom **HCERTSTORE** -Member angegebenen Speicher geprüft.</span><span class="sxs-lookup"><span data-stu-id="3641c-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="3641c-116">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3641c-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="3641c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3641c-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="3641c-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3641c-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="3641c-119"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="3641c-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="3641c-120">Fügen Sie nur Zertifikate in der Zertifikat Kette hinzu.</span><span class="sxs-lookup"><span data-stu-id="3641c-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="3641c-121"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette \_ ohne \_**</dt> Stamm <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="3641c-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="3641c-122">Fügen Sie nur Zertifikate in der Zertifikat Kette mit Ausnahme des Stamm Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="3641c-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="3641c-123"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Speicher**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="3641c-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="3641c-124">Fügen Sie alle Zertifikate in dem Speicher hinzu, der vom **HCERTSTORE** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3641c-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="3641c-125">Dieses Flag kann eine bitweise **or** -Kombination mit einem der anderen möglichen Werte für diesen Member sein.</span><span class="sxs-lookup"><span data-stu-id="3641c-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3641c-126">**HCERTSTORE**</span><span class="sxs-lookup"><span data-stu-id="3641c-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="3641c-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="3641c-127">Optional.</span></span> <span data-ttu-id="3641c-128">Ein Handle für einen zusätzlichen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="3641c-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3641c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3641c-129">Requirements</span></span>



| <span data-ttu-id="3641c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3641c-130">Requirement</span></span> | <span data-ttu-id="3641c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3641c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3641c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3641c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3641c-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3641c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3641c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3641c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3641c-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3641c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3641c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3641c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3641c-137">**Signatur Geber \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="3641c-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
