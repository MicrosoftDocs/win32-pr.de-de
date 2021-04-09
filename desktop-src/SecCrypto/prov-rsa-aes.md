---
description: Unterstützt sowohl digitale Signaturen als auch Datenverschlüsselung. Es gilt als allgemeiner Kryptografiedienstanbieter (CSP).
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042690"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="d2b51-104">Prov \_ RSA \_ AES</span><span class="sxs-lookup"><span data-stu-id="d2b51-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="d2b51-105">Der Prov \_ RSA \_ AES-Anbietertyp unterstützt sowohl [digitale Signaturen](digital-signatures.md) als auch Datenverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="d2b51-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="d2b51-106">Es gilt als allgemeiner [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="d2b51-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="d2b51-107">Der RSA- [*Algorithmus für öffentliche*](../secgloss/p-gly.md) Schlüssel wird für alle Vorgänge mit [*öffentlichem Schlüssel*](../secgloss/p-gly.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2b51-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="d2b51-108">Unterstützte Algorithmen</span><span class="sxs-lookup"><span data-stu-id="d2b51-108">Algorithms Supported</span></span>

<span data-ttu-id="d2b51-109">Beschreibungen der einzelnen Algorithmen finden Sie im Glossar.</span><span class="sxs-lookup"><span data-stu-id="d2b51-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="d2b51-110">Zweck</span><span class="sxs-lookup"><span data-stu-id="d2b51-110">Purpose</span></span>      | <span data-ttu-id="d2b51-111">Unterstützte Algorithmen</span><span class="sxs-lookup"><span data-stu-id="d2b51-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b51-112">Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="d2b51-112">Key Exchange</span></span> | [<span data-ttu-id="d2b51-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="d2b51-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="d2b51-114">Signatur</span><span class="sxs-lookup"><span data-stu-id="d2b51-114">Signature</span></span>    | [<span data-ttu-id="d2b51-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="d2b51-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="d2b51-116">Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d2b51-116">Encryption</span></span>   | [<span data-ttu-id="d2b51-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="d2b51-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="d2b51-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="d2b51-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="d2b51-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="d2b51-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="d2b51-120">Hashing</span><span class="sxs-lookup"><span data-stu-id="d2b51-120">Hashing</span></span>      | [<span data-ttu-id="d2b51-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="d2b51-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="d2b51-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="d2b51-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="d2b51-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="d2b51-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="d2b51-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="d2b51-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="d2b51-125">SHA-2 (SHA-256, SHA-384 und SHA-512)</span><span class="sxs-lookup"><span data-stu-id="d2b51-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="d2b51-126">Verwandte Dokumentationen</span><span class="sxs-lookup"><span data-stu-id="d2b51-126">Related Documentation</span></span>

<span data-ttu-id="d2b51-127">Dieser Anbietertyp wird von Microsoft und RSA-Datensicherheit definiert.</span><span class="sxs-lookup"><span data-stu-id="d2b51-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="d2b51-128">Dies wird in den folgenden Dokumenten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="d2b51-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="d2b51-129">*Microsoft Kryptografiedienstanbieter-Programmierer*, Microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="d2b51-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="d2b51-130">RSA-Laboratorien, Kryptografiestandards für öffentliche Schlüssel, RSA-Datensicherheit, November 1993.</span><span class="sxs-lookup"><span data-stu-id="d2b51-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="d2b51-131">Diese Ressourcen sind möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2b51-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
