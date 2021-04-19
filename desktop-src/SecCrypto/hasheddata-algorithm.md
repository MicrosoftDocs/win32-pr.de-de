---
description: Legt den Typ des verwendeten Hash Algorithmus fest oder ruft ihn ab.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData. algorithmuseigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369982"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="c9929-103">HashedData. algorithmuseigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9929-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="c9929-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c9929-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c9929-105">Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c9929-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c9929-106">Die  algorithmuseigenschaft legt den Typ des verwendeten Hash Algorithmus fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c9929-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9929-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9929-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="c9929-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c9929-108">Property value</span></span>

<span data-ttu-id="c9929-109">Ein Wert der [**CAPICOM- \_ Hash \_ Algorithmus**](capicom-hash-algorithm.md) -Enumeration, die einen Hash Algorithmus definiert.</span><span class="sxs-lookup"><span data-stu-id="c9929-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="c9929-110">Der Standardwert ist der CAPICOM- \_ Hash \_ Algorithmus \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="c9929-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="c9929-111">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9929-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="c9929-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c9929-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="c9929-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c9929-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="c9929-114"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="c9929-115">SHA1-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c9929-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="c9929-116"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ MD2**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="c9929-117">MD2-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="c9929-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="c9929-118"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="c9929-119">MD4-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="c9929-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="c9929-120"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="c9929-121">MD5-Hashalgorithmus</span><span class="sxs-lookup"><span data-stu-id="c9929-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="c9929-122"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="c9929-123">SHA-256-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c9929-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="c9929-124">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9929-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="c9929-125"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="c9929-126">SHA-384-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c9929-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="c9929-127">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9929-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="c9929-128"><dt>**CAPICOM- \_ Hash \_ Algorithmus \_ SHA \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="c9929-129">SHA-512-Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="c9929-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="c9929-130">**CAPICOM 2.0.0.3 und früher:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9929-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9929-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9929-131">Requirements</span></span>



| <span data-ttu-id="c9929-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9929-132">Requirement</span></span> | <span data-ttu-id="c9929-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c9929-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9929-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c9929-134">End of client support</span></span><br/> | <span data-ttu-id="c9929-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9929-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c9929-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c9929-136">End of server support</span></span><br/> | <span data-ttu-id="c9929-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9929-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c9929-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c9929-138">Redistributable</span></span><br/>       | <span data-ttu-id="c9929-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9929-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c9929-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c9929-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c9929-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9929-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9929-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9929-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9929-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="c9929-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
