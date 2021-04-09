---
description: Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit größerer Sicherheit als derzeit mit dem Kryptografieanbieter von Microsoft. Eine größere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Vergleich der Schlüssellänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869012"
---
# <a name="key-length-comparison"></a><span data-ttu-id="b031f-104">Vergleich der Schlüssellänge</span><span class="sxs-lookup"><span data-stu-id="b031f-104">Key Length Comparison</span></span>

<span data-ttu-id="b031f-105">Der Microsoft Enhanced Cryptographic Provider bietet eine Anwendung mit größerer Sicherheit als derzeit mit dem Kryptografieanbieter von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b031f-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="b031f-106">Eine größere Schlüssellänge bietet Benutzern mehr Schutz für sensible Daten.</span><span class="sxs-lookup"><span data-stu-id="b031f-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="b031f-107">In der folgenden Tabelle werden die Standard [*Schlüssellängen*](../secgloss/k-gly.md) aufgelistet, die vom Basis Anbieter und dem erweiterten Anbieter für Standardalgorithmen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b031f-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="b031f-108">Algorithmus</span><span class="sxs-lookup"><span data-stu-id="b031f-108">Algorithm</span></span>                                                                                | <span data-ttu-id="b031f-109">Basis Anbieter</span><span class="sxs-lookup"><span data-stu-id="b031f-109">Base Provider</span></span> | <span data-ttu-id="b031f-110">Starke und erweiterte Anbieter</span><span class="sxs-lookup"><span data-stu-id="b031f-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="b031f-111">RSA-Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="b031f-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="b031f-112">512-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-112">512-bit</span></span>       | <span data-ttu-id="b031f-113">1.024-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-113">1,024-bit</span></span>                     |
| <span data-ttu-id="b031f-114">RSA-Signatur</span><span class="sxs-lookup"><span data-stu-id="b031f-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="b031f-115">512-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-115">512-bit</span></span>       | <span data-ttu-id="b031f-116">1.024-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-116">1,024-bit</span></span>                     |
| <span data-ttu-id="b031f-117">RC2</span><span class="sxs-lookup"><span data-stu-id="b031f-117">RC2</span></span>                                                                                      | <span data-ttu-id="b031f-118">40-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-118">40-bit</span></span>        | <span data-ttu-id="b031f-119">128 Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-119">128-bit</span></span>                       |
| <span data-ttu-id="b031f-120">RC4</span><span class="sxs-lookup"><span data-stu-id="b031f-120">RC4</span></span>                                                                                      | <span data-ttu-id="b031f-121">40-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-121">40-bit</span></span>        | <span data-ttu-id="b031f-122">128 Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-122">128-bit</span></span>                       |
| <span data-ttu-id="b031f-123">DES</span><span class="sxs-lookup"><span data-stu-id="b031f-123">DES</span></span>                                                                                      | <span data-ttu-id="b031f-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b031f-124">Not supported</span></span> | <span data-ttu-id="b031f-125">56-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-125">56-bit</span></span>                        |
| <span data-ttu-id="b031f-126">[*Triple des*](../secgloss/t-gly.md) (2-Taste)</span><span class="sxs-lookup"><span data-stu-id="b031f-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="b031f-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b031f-127">Not supported</span></span> | <span data-ttu-id="b031f-128">112-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-128">112-bit</span></span>                       |
| <span data-ttu-id="b031f-129">Triple des (3-Taste)</span><span class="sxs-lookup"><span data-stu-id="b031f-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="b031f-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b031f-130">Not supported</span></span> | <span data-ttu-id="b031f-131">168-Bit</span><span class="sxs-lookup"><span data-stu-id="b031f-131">168-bit</span></span>                       |



 

<span data-ttu-id="b031f-132">Der [*-und*](../secgloss/d-gly.md) der [*Triple des*](../secgloss/t-gly.md) -Algorithmen werden im erweiterten Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b031f-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="b031f-133">Der erweiterte Anbieter ist abwärts kompatibel mit dem Basis Anbieter, der mit früheren Versionen der CryptoAPI verteilt wurde, mit der folgenden Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="b031f-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="b031f-134">Sowohl der Basis Anbieter als auch der erweiterte Anbieter können nur Sitzungsschlüssel der Standard Schlüssellänge generieren.</span><span class="sxs-lookup"><span data-stu-id="b031f-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="b031f-135">Die Standardlänge der Sitzungsschlüssel für den Basis Anbieter beträgt 40 Bits.</span><span class="sxs-lookup"><span data-stu-id="b031f-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="b031f-136">Die Standardschlüssel Länge für den erweiterten Anbieter beträgt 128 Bits.</span><span class="sxs-lookup"><span data-stu-id="b031f-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="b031f-137">Der erweiterte Anbieter kann keine Schlüssel mit Basis Anbieter kompatiblen Schlüssellängen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b031f-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="b031f-138">Der erweiterte Anbieter kann jedoch Schlüssellängen beliebiger Größe (bis zu 128 Bits) importieren.</span><span class="sxs-lookup"><span data-stu-id="b031f-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
