---
description: Definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: CAPICOM_ENCRYPTION_ALGORITHM-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368536"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="dc484-103">CAPICOM- \_ Verschlüsselungs \_ Algorithmus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="dc484-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="dc484-104">Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Algorithmus** " definiert die Algorithmen, die bei der Verschlüsselung und Entschlüsselung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc484-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="dc484-105">Member</span><span class="sxs-lookup"><span data-stu-id="dc484-105">Members</span></span>



| <span data-ttu-id="dc484-106">Member</span><span class="sxs-lookup"><span data-stu-id="dc484-106">Member</span></span>                                   | <span data-ttu-id="dc484-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc484-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="dc484-108">Wert</span><span class="sxs-lookup"><span data-stu-id="dc484-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="dc484-109">**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="dc484-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="dc484-110">Verwenden Sie die RSA RC2-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="dc484-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="dc484-111">0</span><span class="sxs-lookup"><span data-stu-id="dc484-111">0</span></span>         |
| <span data-ttu-id="dc484-112">**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="dc484-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="dc484-113">Verwenden Sie die RSA RC4-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="dc484-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="dc484-114">1</span><span class="sxs-lookup"><span data-stu-id="dc484-114">1</span></span>         |
| <span data-ttu-id="dc484-115">**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ des**</span><span class="sxs-lookup"><span data-stu-id="dc484-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="dc484-116">Verwenden Sie die des-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="dc484-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="dc484-117">2</span><span class="sxs-lookup"><span data-stu-id="dc484-117">2</span></span>         |
| <span data-ttu-id="dc484-118">**CAPICOM \_ \_ -Verschlüsselungsalgorithmus \_ 3DES**</span><span class="sxs-lookup"><span data-stu-id="dc484-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="dc484-119">Verwenden Sie die Triple des-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="dc484-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="dc484-120">3</span><span class="sxs-lookup"><span data-stu-id="dc484-120">3</span></span>         |
| <span data-ttu-id="dc484-121">**CAPICOM- \_ Verschlüsselungs \_ Algorithmus \_ AES**</span><span class="sxs-lookup"><span data-stu-id="dc484-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="dc484-122">Verwenden Sie den [*Advanced Encryption Standard*](../secgloss/a-gly.md) -Algorithmus (AES).</span><span class="sxs-lookup"><span data-stu-id="dc484-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="dc484-123">Dieser Wert gilt nur für das Objekt " [**verschlüsselteddata**](encrypteddata.md) ".</span><span class="sxs-lookup"><span data-stu-id="dc484-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="dc484-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="dc484-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="dc484-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc484-125">Remarks</span></span>

<span data-ttu-id="dc484-126">Der Enumerationstyp des **CAPICOM- \_ Verschlüsselungs \_ Algorithmus** wird von der [**Algorithm.Name**](algorithm-name.md) -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc484-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc484-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc484-127">Requirements</span></span>



| <span data-ttu-id="dc484-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc484-128">Requirement</span></span> | <span data-ttu-id="dc484-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dc484-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc484-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dc484-130">Redistributable</span></span><br/> | <span data-ttu-id="dc484-131">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc484-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="dc484-132">Header</span><span class="sxs-lookup"><span data-stu-id="dc484-132">Header</span></span><br/>          | <dl> <span data-ttu-id="dc484-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc484-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
