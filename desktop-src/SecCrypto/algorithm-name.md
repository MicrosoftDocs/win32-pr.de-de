---
description: Legt den Algorithmus fest, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird, oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369549"
---
# <a name="algorithmname-property"></a><span data-ttu-id="305d1-104">Algorithm.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="305d1-104">Algorithm.Name property</span></span>

<span data-ttu-id="305d1-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="305d1-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="305d1-106">Verwenden Sie stattdessen die [**AlgorithmIdentifier-Klasse**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="305d1-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="305d1-107">Die **Name** -Eigenschaft legt den Algorithmus fest, der zum Signieren, umbrechen und Verschlüsseln von Vorgängen verwendet wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="305d1-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="305d1-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="305d1-108">This is the default property.</span></span>

<span data-ttu-id="305d1-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="305d1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="305d1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="305d1-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="305d1-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="305d1-111">Property value</span></span>

<span data-ttu-id="305d1-112">Ein Wert der [**CAPICOM- \_ Verschlüsselungs \_ Algorithmus**](capicom-encryption-algorithm.md) -Enumeration, der angibt, welcher Algorithmus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="305d1-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="305d1-113">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="305d1-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="305d1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="305d1-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="305d1-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="305d1-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="305d1-116"><dt>**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="305d1-117">Verwenden Sie die RC2-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="305d1-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="305d1-118"><dt>**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="305d1-119">Verwenden Sie die RC4-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="305d1-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="305d1-120"><dt>**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ des**</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="305d1-121">Verwenden Sie die des-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="305d1-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="305d1-122"><dt>**CAPICOM \_ \_ -Verschlüsselungsalgorithmus \_ 3DES**</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="305d1-123">Verwenden Sie die Triple des-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="305d1-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="305d1-124"><dt>**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="305d1-125">Verwenden Sie den AES-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="305d1-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="305d1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="305d1-126">Remarks</span></span>

<span data-ttu-id="305d1-127">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte Status des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="305d1-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="305d1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="305d1-128">Requirements</span></span>



| <span data-ttu-id="305d1-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="305d1-129">Requirement</span></span> | <span data-ttu-id="305d1-130">Wert</span><span class="sxs-lookup"><span data-stu-id="305d1-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="305d1-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="305d1-131">End of client support</span></span><br/> | <span data-ttu-id="305d1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="305d1-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="305d1-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="305d1-133">End of server support</span></span><br/> | <span data-ttu-id="305d1-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="305d1-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="305d1-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="305d1-135">Redistributable</span></span><br/>       | <span data-ttu-id="305d1-136">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="305d1-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="305d1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="305d1-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="305d1-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="305d1-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
