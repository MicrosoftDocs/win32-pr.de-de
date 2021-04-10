---
description: Vordefinierte Konstanten für Kryptografieprotokolle. Diese Werte sind in Wincrypt. h definiert.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Protokollflags (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960373"
---
# <a name="protocol-flags"></a><span data-ttu-id="8101f-104">Protokollflags</span><span class="sxs-lookup"><span data-stu-id="8101f-104">Protocol Flags</span></span>

<span data-ttu-id="8101f-105">Im folgenden finden Sie vordefinierte Konstanten für Kryptografieprotokolle.</span><span class="sxs-lookup"><span data-stu-id="8101f-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="8101f-106">Diese Werte sind in Wincrypt. h definiert.</span><span class="sxs-lookup"><span data-stu-id="8101f-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="8101f-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="8101f-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="8101f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8101f-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="8101f-109"><dt>**Crypt \_ Flag für \_ IPSec**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="8101f-110">IPSec-Protokoll (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="8101f-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="8101f-111"><dt>**Crypt \_ Flag \_ das PCT1 verwendet**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="8101f-112">PCT-Protokoll (private Communications Transport).</span><span class="sxs-lookup"><span data-stu-id="8101f-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="8101f-113"><dt>**Crypt \_ Flag zum \_ Signieren**</dt> von <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="8101f-114">Signatur Protokoll.</span><span class="sxs-lookup"><span data-stu-id="8101f-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="8101f-115"><dt>**Crypt \_ Flag \_ SSL2 verwendet**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="8101f-116">SSL (Secure Sockets Layer)-Protokoll, Version 2.</span><span class="sxs-lookup"><span data-stu-id="8101f-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="8101f-117"><dt>**Crypt \_ Flag \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="8101f-118">SSL-Protokoll, Version 3.</span><span class="sxs-lookup"><span data-stu-id="8101f-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="8101f-119"><dt>**Crypt \_ Flag \_ das TLS1 verwendet**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="8101f-120">TLS-Protokoll (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="8101f-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="8101f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8101f-121">Requirements</span></span>



| <span data-ttu-id="8101f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8101f-122">Requirement</span></span> | <span data-ttu-id="8101f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8101f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8101f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8101f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8101f-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8101f-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8101f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8101f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8101f-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8101f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8101f-128">Header</span><span class="sxs-lookup"><span data-stu-id="8101f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8101f-129"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="8101f-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8101f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8101f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8101f-131">**Prov- \_ enumalgs ( \_ Ex)**</span><span class="sxs-lookup"><span data-stu-id="8101f-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




