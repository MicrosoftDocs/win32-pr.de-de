---
description: In der folgenden Tabelle sind die Algorithmen aufgelistet, die vom Microsoft DSS-Kryptografieanbieter unterstützt werden.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: DSS-Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360528"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="c0cfa-103">DSS-Anbieter Algorithmen</span><span class="sxs-lookup"><span data-stu-id="c0cfa-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="c0cfa-104">In der folgenden Tabelle sind die Algorithmen aufgelistet, die vom Microsoft DSS-Kryptografieanbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="c0cfa-105">Algorithmuskennung</span><span class="sxs-lookup"><span data-stu-id="c0cfa-105">Algorithm ID</span></span>    | <span data-ttu-id="c0cfa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0cfa-106">Description</span></span>                                 | <span data-ttu-id="c0cfa-107">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c0cfa-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cfa-108">Calg \_ MD5</span><span class="sxs-lookup"><span data-stu-id="c0cfa-108">CALG\_MD5</span></span>       | <span data-ttu-id="c0cfa-109">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="c0cfa-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="c0cfa-110">Wird nur für hashung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="c0cfa-111">calg \_ SHA</span><span class="sxs-lookup"><span data-stu-id="c0cfa-111">CALG\_SHA</span></span>       | <span data-ttu-id="c0cfa-112">SHA-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="c0cfa-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="c0cfa-113">Muss für DSS-Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="c0cfa-114">Calg \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="c0cfa-114">CALG\_SHA1</span></span>      | <span data-ttu-id="c0cfa-115">Identisch mit calg \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="c0cfa-116">Kein Kommentar.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="c0cfa-117">calg- \_ DSS- \_ Zeichen</span><span class="sxs-lookup"><span data-stu-id="c0cfa-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="c0cfa-118">DSS-Algorithmus für die öffentliche/private Schlüssel Signatur.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="c0cfa-119">Schlüssellänge: kann festgelegt werden, 512 Bits auf 1.024 Bits in 64-Bit-Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="c0cfa-120">Standard Schlüssellänge: 1.024 Bits.</span><span class="sxs-lookup"><span data-stu-id="c0cfa-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




