---
description: Algorithmen können vom Microsoft RSA/SChannel-Kryptografieanbieter unterstützt werden.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: RSA/SChannel-Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359868"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="6643f-103">RSA/SChannel-Anbieter Algorithmen</span><span class="sxs-lookup"><span data-stu-id="6643f-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="6643f-104">Die folgenden Algorithmen können vom Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Kryptografieanbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6643f-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="6643f-105">Algorithmuskennung</span><span class="sxs-lookup"><span data-stu-id="6643f-105">Algorithm ID</span></span>    | <span data-ttu-id="6643f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6643f-106">Description</span></span>                                                                                                                         | <span data-ttu-id="6643f-107">Kommentare</span><span class="sxs-lookup"><span data-stu-id="6643f-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6643f-108">calg \_ RSA \_ Keyx</span><span class="sxs-lookup"><span data-stu-id="6643f-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="6643f-109">RSA-Algorithmus für den [ *Schlüsselaustausch* von öffentlichem Schlüssel](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="6643f-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="6643f-110">Schlüssellänge: kann festgelegt werden, 384 Bits auf 16.384 Bits in 8-Bit-Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="6643f-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="6643f-111">Standard Schlüssellänge: 1.024 Bits.</span><span class="sxs-lookup"><span data-stu-id="6643f-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="6643f-112">Calg \_ MD5</span><span class="sxs-lookup"><span data-stu-id="6643f-112">CALG\_MD5</span></span>       | <span data-ttu-id="6643f-113">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="6643f-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="6643f-114">Wird nur für hashung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6643f-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="6643f-115">calg \_ SHA</span><span class="sxs-lookup"><span data-stu-id="6643f-115">CALG\_SHA</span></span>       | <span data-ttu-id="6643f-116">SHA-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="6643f-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="6643f-117">Muss für DSS-Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6643f-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="6643f-118">Calg \_ RC2</span><span class="sxs-lookup"><span data-stu-id="6643f-118">CALG\_RC2</span></span>       | <span data-ttu-id="6643f-119">RC2-Block Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="6643f-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="6643f-120">Schlüssellänge: 40 bis 88 Bits</span><span class="sxs-lookup"><span data-stu-id="6643f-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="6643f-121">Calg \_ RC4</span><span class="sxs-lookup"><span data-stu-id="6643f-121">CALG\_RC4</span></span>       | <span data-ttu-id="6643f-122">RC4-Stream-Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="6643f-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="6643f-123">Schlüssellänge: 40 bis 88 Bits</span><span class="sxs-lookup"><span data-stu-id="6643f-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
