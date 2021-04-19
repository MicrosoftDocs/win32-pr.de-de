---
description: Gibt den Zertifikat Speicher an, der zum Signieren eines Dokuments verwendet wird.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: SIGNER_CERT_STORE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348220"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="05f84-103">Signatur Geber- \_ Zertifikat \_ Speicher Info- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="05f84-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="05f84-104">Die Signatur Geber-Zertifikat **\_ \_ \_ Informations** Struktur gibt den Zertifikat Speicher an, der zum Signieren eines Dokuments verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05f84-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="05f84-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="05f84-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="05f84-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="05f84-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="05f84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05f84-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="05f84-108">Member</span><span class="sxs-lookup"><span data-stu-id="05f84-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="05f84-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="05f84-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="05f84-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="05f84-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="05f84-111">**psigningcert**</span><span class="sxs-lookup"><span data-stu-id="05f84-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="05f84-112">Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur für das Signaturzertifikat.</span><span class="sxs-lookup"><span data-stu-id="05f84-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="05f84-113">**dwcertpolicy**</span><span class="sxs-lookup"><span data-stu-id="05f84-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="05f84-114">Gibt an, wie der Signatur Zertifikate hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="05f84-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="05f84-115">Zum Ermitteln der Zertifikat Kette werden die Speicher "My", "ca", "root" und "SPC" zusätzlich zu dem vom **HCERTSTORE** -Member angegebenen Speicher geprüft.</span><span class="sxs-lookup"><span data-stu-id="05f84-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="05f84-116">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="05f84-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="05f84-117">Wert</span><span class="sxs-lookup"><span data-stu-id="05f84-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="05f84-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="05f84-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="05f84-119"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="05f84-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="05f84-120">Fügen Sie nur Zertifikate in der Zertifikat Kette hinzu.</span><span class="sxs-lookup"><span data-stu-id="05f84-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="05f84-121"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette \_ ohne \_**</dt> Stamm <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="05f84-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="05f84-122">Fügen Sie nur Zertifikate in der Zertifikat Kette mit Ausnahme des Stamm Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="05f84-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="05f84-123"><dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Speicher**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="05f84-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="05f84-124">Fügen Sie alle Zertifikate in dem Speicher hinzu, der vom **HCERTSTORE** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05f84-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="05f84-125">Dieses Flag kann eine bitweise **or** -Kombination mit einem der anderen möglichen Werte für diesen Member sein.</span><span class="sxs-lookup"><span data-stu-id="05f84-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="05f84-126">**HCERTSTORE**</span><span class="sxs-lookup"><span data-stu-id="05f84-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="05f84-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="05f84-127">Optional.</span></span> <span data-ttu-id="05f84-128">Ein Handle für einen zusätzlichen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="05f84-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05f84-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05f84-129">Requirements</span></span>



| <span data-ttu-id="05f84-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05f84-130">Requirement</span></span> | <span data-ttu-id="05f84-131">Wert</span><span class="sxs-lookup"><span data-stu-id="05f84-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05f84-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05f84-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05f84-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05f84-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="05f84-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05f84-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05f84-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05f84-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05f84-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05f84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f84-137">**Signatur Geber \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="05f84-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




