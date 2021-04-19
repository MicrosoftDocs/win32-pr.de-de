---
description: Von Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter unterstützte Algorithmen.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: PROV_DSS_DH Anbieter Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366494"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="08af4-103">Prov- \_ DSS- \_ dh-Anbieter Algorithmen</span><span class="sxs-lookup"><span data-stu-id="08af4-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="08af4-104">In der folgenden Tabelle werden die Algorithmen aufgelistet, die vom Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="08af4-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="08af4-105">Algorithmuskennung</span><span class="sxs-lookup"><span data-stu-id="08af4-105">Algorithm ID</span></span>      | <span data-ttu-id="08af4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08af4-106">Description</span></span>                                 | <span data-ttu-id="08af4-107">Kommentare</span><span class="sxs-lookup"><span data-stu-id="08af4-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08af4-108">Calg \_ MD5</span><span class="sxs-lookup"><span data-stu-id="08af4-108">CALG\_MD5</span></span>         | <span data-ttu-id="08af4-109">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="08af4-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="08af4-110">Wird nur für hashung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08af4-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="08af4-111">calg \_ SHA</span><span class="sxs-lookup"><span data-stu-id="08af4-111">CALG\_SHA</span></span>         | <span data-ttu-id="08af4-112">SHA-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="08af4-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="08af4-113">Muss für DSS-Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08af4-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="08af4-114">Calg \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="08af4-114">CALG\_SHA1</span></span>        | <span data-ttu-id="08af4-115">Identisch mit calg \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="08af4-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="08af4-116">Kein Kommentar.</span><span class="sxs-lookup"><span data-stu-id="08af4-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="08af4-117">calg- \_ DSS- \_ Zeichen</span><span class="sxs-lookup"><span data-stu-id="08af4-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="08af4-118">DSS-Algorithmus für die öffentliche/private Schlüssel Signatur.</span><span class="sxs-lookup"><span data-stu-id="08af4-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="08af4-119">Schlüssellänge: kann festgelegt werden, 512 Bits auf 1.024 Bits in 64-Bit-Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="08af4-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="08af4-120">Standard Schlüssellänge: 1.024 Bits.</span><span class="sxs-lookup"><span data-stu-id="08af4-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="08af4-121">"calg \_ dh \_ SF"</span><span class="sxs-lookup"><span data-stu-id="08af4-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="08af4-122">Speichern und Weiterleiten von D-H-Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="08af4-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="08af4-123">Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="08af4-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="08af4-124">Standard Schlüssellänge: 512 Bits.</span><span class="sxs-lookup"><span data-stu-id="08af4-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="08af4-125">calg \_ dh- \_ ephem</span><span class="sxs-lookup"><span data-stu-id="08af4-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="08af4-126">Kurzlebiger D-H-Schlüsselaustausch.</span><span class="sxs-lookup"><span data-stu-id="08af4-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="08af4-127">Schlüssellänge: kann festgelegt werden, 384 Bits auf 512 Bits in 8-Bit-Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="08af4-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="08af4-128">Standard Schlüssellänge: 512 Bits.</span><span class="sxs-lookup"><span data-stu-id="08af4-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="08af4-129">calg \_ Cylink \_ MEK</span><span class="sxs-lookup"><span data-stu-id="08af4-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="08af4-130">Eine 40-Bit-Variante eines des-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="08af4-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="08af4-131">Schlüssellänge: 40 Bits.</span><span class="sxs-lookup"><span data-stu-id="08af4-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




