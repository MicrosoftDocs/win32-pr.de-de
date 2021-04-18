---
description: Die CAPICOM- \_ Hash \_ Algorithmus-Enumeration definiert einen Hash Algorithmus.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: CAPICOM_HASH_ALGORITHM-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368413"
---
# <a name="capicom_hash_algorithm-enumeration"></a><span data-ttu-id="825f9-103">CAPICOM- \_ Hash \_ Algorithmus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="825f9-103">CAPICOM\_HASH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="825f9-104">Die **CAPICOM- \_ Hash \_ Algorithmus** -Enumeration definiert einen Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="825f9-104">The **CAPICOM\_HASH\_ALGORITHM** enumeration defines a hash algorithm.</span></span>

## <a name="members"></a><span data-ttu-id="825f9-105">Member</span><span class="sxs-lookup"><span data-stu-id="825f9-105">Members</span></span>



| <span data-ttu-id="825f9-106">Member</span><span class="sxs-lookup"><span data-stu-id="825f9-106">Member</span></span>                                 | <span data-ttu-id="825f9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="825f9-107">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="825f9-108">Wert</span><span class="sxs-lookup"><span data-stu-id="825f9-108">Value</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="825f9-109">**CAPICOM- \_ Hash \_ Algorithmus \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="825f9-109">**CAPICOM\_HASH\_ALGORITHM\_SHA1**</span></span>     | <span data-ttu-id="825f9-110">[*Secure Hash-Algorithmus*](../secgloss/s-gly.md) (SHA), der einen 160-Bit-Nachrichten Digest generiert.</span><span class="sxs-lookup"><span data-stu-id="825f9-110">[*Secure Hash Algorithm*](../secgloss/s-gly.md) (SHA) that generates a 160-bit message digest.</span></span><br/> | <span data-ttu-id="825f9-111">0</span><span class="sxs-lookup"><span data-stu-id="825f9-111">0</span></span>     |
| <span data-ttu-id="825f9-112">**CAPICOM- \_ Hash \_ Algorithmus \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="825f9-112">**CAPICOM\_HASH\_ALGORITHM\_MD2**</span></span>      | <span data-ttu-id="825f9-113">MD2-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="825f9-113">MD2 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="825f9-114">1</span><span class="sxs-lookup"><span data-stu-id="825f9-114">1</span></span>     |
| <span data-ttu-id="825f9-115">**CAPICOM- \_ Hash \_ Algorithmus \_ MD4**</span><span class="sxs-lookup"><span data-stu-id="825f9-115">**CAPICOM\_HASH\_ALGORITHM\_MD4**</span></span>      | <span data-ttu-id="825f9-116">MD4-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="825f9-116">MD4 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="825f9-117">2</span><span class="sxs-lookup"><span data-stu-id="825f9-117">2</span></span>     |
| <span data-ttu-id="825f9-118">**CAPICOM- \_ Hash \_ Algorithmus \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="825f9-118">**CAPICOM\_HASH\_ALGORITHM\_MD5**</span></span>      | <span data-ttu-id="825f9-119">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="825f9-119">MD5 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="825f9-120">3</span><span class="sxs-lookup"><span data-stu-id="825f9-120">3</span></span>     |
| <span data-ttu-id="825f9-121">**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 256**</span><span class="sxs-lookup"><span data-stu-id="825f9-121">**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</span></span> | <span data-ttu-id="825f9-122">SHA-256-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="825f9-122">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="825f9-123">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825f9-123">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="825f9-124">4</span><span class="sxs-lookup"><span data-stu-id="825f9-124">4</span></span>     |
| <span data-ttu-id="825f9-125">**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 384**</span><span class="sxs-lookup"><span data-stu-id="825f9-125">**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</span></span> | <span data-ttu-id="825f9-126">SHA-384-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="825f9-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="825f9-127">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825f9-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="825f9-128">5</span><span class="sxs-lookup"><span data-stu-id="825f9-128">5</span></span>     |
| <span data-ttu-id="825f9-129">**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 512**</span><span class="sxs-lookup"><span data-stu-id="825f9-129">**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</span></span> | <span data-ttu-id="825f9-130">SHA-512-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="825f9-130">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="825f9-131">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825f9-131">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="825f9-132">6</span><span class="sxs-lookup"><span data-stu-id="825f9-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="825f9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="825f9-133">Remarks</span></span>

<span data-ttu-id="825f9-134">Die **CAPICOM- \_ Hash \_ Algorithmus** -Enumeration wird von der [**hashedData. algorithmuseigenschaft**](hasheddata-algorithm.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="825f9-134">The **CAPICOM\_HASH\_ALGORITHM** enumeration is used by the [**HashedData.Algorithm**](hasheddata-algorithm.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="825f9-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="825f9-135">Requirements</span></span>



| <span data-ttu-id="825f9-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="825f9-136">Requirement</span></span> | <span data-ttu-id="825f9-137">Wert</span><span class="sxs-lookup"><span data-stu-id="825f9-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="825f9-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="825f9-138">Redistributable</span></span><br/> | <span data-ttu-id="825f9-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="825f9-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="825f9-140">Header</span><span class="sxs-lookup"><span data-stu-id="825f9-140">Header</span></span><br/>          | <dl> <span data-ttu-id="825f9-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="825f9-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 
