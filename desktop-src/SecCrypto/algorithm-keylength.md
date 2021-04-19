---
description: Legt die Länge des Schlüssels fest oder ruft diese ab.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Algorithmus. keylength-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369378"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="6268a-103">Algorithmus. keylength-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6268a-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="6268a-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6268a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="6268a-105">Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="6268a-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6268a-106">Die **keylength** -Eigenschaft legt die Länge des Schlüssels fest oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="6268a-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="6268a-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6268a-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6268a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6268a-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="6268a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6268a-109">Property value</span></span>

<span data-ttu-id="6268a-110">Ein Wert der-Enumeration der [**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge**](capicom-encryption-key-length.md) , die die Schlüssellänge angibt.</span><span class="sxs-lookup"><span data-stu-id="6268a-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="6268a-111">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6268a-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="6268a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6268a-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="6268a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6268a-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="6268a-114"><dt>**\_ \_ \_ \_ maximal zulässige Länge von CAPICOM-Verschlüsselungsschlüsseln**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="6268a-115">Verwenden Sie die maximale Schlüssellänge, die mit dem angegeben Verschlüsselungsalgorithmus verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6268a-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="6268a-116"><dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 40 \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="6268a-117">Verwenden Sie 40-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6268a-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="6268a-118"><dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 56 \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="6268a-119">Verwenden Sie bei Verfügbarkeit 56-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6268a-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="6268a-120"><dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 128 \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="6268a-121">Verwenden Sie bei Verfügbarkeit 128-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6268a-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="6268a-122"><dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 192 \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="6268a-123">Verwenden Sie 192-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6268a-123">Use 192-bit keys.</span></span> <span data-ttu-id="6268a-124">Diese Schlüssellänge ist nur für AES verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6268a-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="6268a-125"><dt>**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 256 \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="6268a-126">Verwenden Sie 256-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6268a-126">Use 256-bit keys.</span></span> <span data-ttu-id="6268a-127">Diese Schlüssellänge ist nur für AES verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6268a-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6268a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6268a-128">Remarks</span></span>

<span data-ttu-id="6268a-129">Wenn der-und 3DES-Verschlüsselungsalgorithmen verwendet werden, sind die Schlüssellängen Standard, und die **keylength** -Eigenschaft wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6268a-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6268a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6268a-130">Requirements</span></span>



| <span data-ttu-id="6268a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6268a-131">Requirement</span></span> | <span data-ttu-id="6268a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6268a-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6268a-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6268a-133">End of client support</span></span><br/> | <span data-ttu-id="6268a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6268a-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6268a-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6268a-135">End of server support</span></span><br/> | <span data-ttu-id="6268a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6268a-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6268a-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6268a-137">Redistributable</span></span><br/>       | <span data-ttu-id="6268a-138">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6268a-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6268a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6268a-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6268a-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6268a-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6268a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6268a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6268a-142">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="6268a-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
