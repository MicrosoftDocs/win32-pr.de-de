---
description: Unterstützte Protokolle und Verschlüsselungs Sammlungen können mithilfe von Aufrufen von CryptGetProvParam mit PP \_ enumalgs oder PP \_ enumalgs Ex aufgelistet werden \_ .
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Auflisten unterstützter Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372989"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="b2c1e-103">Auflisten unterstützter Protokolle</span><span class="sxs-lookup"><span data-stu-id="b2c1e-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="b2c1e-104">Unterstützte Protokolle und Verschlüsselungs Sammlungen können mithilfe von Aufrufen von [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit PP \_ enumalgs oder PP \_ enumalgs Ex aufgelistet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="b2c1e-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="b2c1e-105">Der Wert "PP \_ enumalgs \_ Ex" funktioniert wie PP- \_ enumalgs, gibt jedoch eine [**Prov \_ enumalgs \_ Ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) -Struktur zurück, die ausführlichere Informationen zu den vom Anbieter unterstützten Algorithmen enthält.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="b2c1e-106">Weitere Informationen zu definierten protokollflags und deren Werten finden Sie unter [protokollflags](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b2c1e-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="b2c1e-107">Da das **hcryptprov** -Element das [*handle*](../secgloss/h-gly.md) eines offenen Kryptografiekontexts ist, der mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) abgerufen wurde, dessen *dwprovtype* -Parameter auf Prov RSA SChannel festgelegt ist [](../secgloss/c-gly.md) \_ \_ , werden im folgenden Beispiel die Namen aller im CSP verfügbaren Algorithmen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="b2c1e-108">In der folgenden Tabelle werden einige Algorithmen aufgelistet, die von einem typischen in der Standard- \_ RSA \_ SChannel-CSP zurückgegebenen Algorithmus</span><span class="sxs-lookup"><span data-stu-id="b2c1e-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="b2c1e-109">Beachten Sie, dass in diesem Beispiel weder SSL2 verwendet SHA Macs noch SSL2 verwendet der-Verschlüsselung vom CSP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="b2c1e-110">Algorithmusbezeichner</span><span class="sxs-lookup"><span data-stu-id="b2c1e-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="b2c1e-111">Minimale Schlüssellänge</span><span class="sxs-lookup"><span data-stu-id="b2c1e-111">Minimum key length</span></span> | <span data-ttu-id="b2c1e-112">Maximale Schlüssellänge</span><span class="sxs-lookup"><span data-stu-id="b2c1e-112">Maximum key length</span></span> | <span data-ttu-id="b2c1e-113">Protokolle</span><span class="sxs-lookup"><span data-stu-id="b2c1e-113">Protocols</span></span> | <span data-ttu-id="b2c1e-114">Algorithmusname</span><span class="sxs-lookup"><span data-stu-id="b2c1e-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="b2c1e-115">*calg \_ RSA \_ Keyx*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="b2c1e-116">512</span><span class="sxs-lookup"><span data-stu-id="b2c1e-116">512</span></span>                | <span data-ttu-id="b2c1e-117">2048</span><span class="sxs-lookup"><span data-stu-id="b2c1e-117">2048</span></span>               | <span data-ttu-id="b2c1e-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="b2c1e-118">0x0007</span></span>    | <span data-ttu-id="b2c1e-119">"RSA \_ Keyx"</span><span class="sxs-lookup"><span data-stu-id="b2c1e-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="b2c1e-120">*Calg \_ MD5*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b2c1e-121">128</span><span class="sxs-lookup"><span data-stu-id="b2c1e-121">128</span></span>                | <span data-ttu-id="b2c1e-122">128</span><span class="sxs-lookup"><span data-stu-id="b2c1e-122">128</span></span>                | <span data-ttu-id="b2c1e-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="b2c1e-123">0x0007</span></span>    | <span data-ttu-id="b2c1e-124">Benutzen</span><span class="sxs-lookup"><span data-stu-id="b2c1e-124">"MD5"</span></span>          |
| [<span data-ttu-id="b2c1e-125">*calg \_ SHA*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b2c1e-126">160</span><span class="sxs-lookup"><span data-stu-id="b2c1e-126">160</span></span>                | <span data-ttu-id="b2c1e-127">160</span><span class="sxs-lookup"><span data-stu-id="b2c1e-127">160</span></span>                | <span data-ttu-id="b2c1e-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="b2c1e-128">0x0005</span></span>    | <span data-ttu-id="b2c1e-129">SHA</span><span class="sxs-lookup"><span data-stu-id="b2c1e-129">"SHA"</span></span>          |
| [<span data-ttu-id="b2c1e-130">*Calg \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b2c1e-131">40</span><span class="sxs-lookup"><span data-stu-id="b2c1e-131">40</span></span>                 | <span data-ttu-id="b2c1e-132">128</span><span class="sxs-lookup"><span data-stu-id="b2c1e-132">128</span></span>                | <span data-ttu-id="b2c1e-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="b2c1e-133">0x0007</span></span>    | <span data-ttu-id="b2c1e-134">RC4</span><span class="sxs-lookup"><span data-stu-id="b2c1e-134">"RC4"</span></span>          |
| <span data-ttu-id="b2c1e-135">" \_ calg"</span><span class="sxs-lookup"><span data-stu-id="b2c1e-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="b2c1e-136">56</span><span class="sxs-lookup"><span data-stu-id="b2c1e-136">56</span></span>                 | <span data-ttu-id="b2c1e-137">56</span><span class="sxs-lookup"><span data-stu-id="b2c1e-137">56</span></span>                 | <span data-ttu-id="b2c1e-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="b2c1e-138">0x0005</span></span>    | <span data-ttu-id="b2c1e-139">DES</span><span class="sxs-lookup"><span data-stu-id="b2c1e-139">"DES"</span></span>          |



 

<span data-ttu-id="b2c1e-140">Um das Senden von ClientHello-oder serverhello-Nachrichten vorzubereiten, listet die [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine die vom CSP unterstützten Algorithmen und Schlüsselgrößen auf und erstellt intern eine Liste der unterstützten Verschlüsselungs Sammlungen.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
