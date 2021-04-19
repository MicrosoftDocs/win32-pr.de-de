---
description: Definiert die Schlüssellänge, die bei der Verschlüsselung verwendet werden soll.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: CAPICOM_ENCRYPTION_KEY_LENGTH-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367848"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="0e659-103">CAPICOM- \_ Verschlüsselungs \_ Schlüssellänge- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="0e659-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="0e659-104">Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge** " definiert die [*Schlüssellänge*](../secgloss/k-gly.md) , die bei der Verschlüsselung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e659-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="0e659-105">Member</span><span class="sxs-lookup"><span data-stu-id="0e659-105">Members</span></span>



| <span data-ttu-id="0e659-106">Member</span><span class="sxs-lookup"><span data-stu-id="0e659-106">Member</span></span>                                          | <span data-ttu-id="0e659-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e659-107">Description</span></span>                                                                               | <span data-ttu-id="0e659-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0e659-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0e659-109">**\_ \_ \_ \_ maximal zulässige Länge von CAPICOM-Verschlüsselungsschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="0e659-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="0e659-110">Verwendet die maximale Schlüssellänge, die mit dem angegeben Verschlüsselungsalgorithmus verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0e659-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="0e659-111">0</span><span class="sxs-lookup"><span data-stu-id="0e659-111">0</span></span>         |
| <span data-ttu-id="0e659-112">**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 40 \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="0e659-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="0e659-113">Verwendet 40-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0e659-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="0e659-114">1</span><span class="sxs-lookup"><span data-stu-id="0e659-114">1</span></span>         |
| <span data-ttu-id="0e659-115">**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 56 \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="0e659-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="0e659-116">Verwendet 56-Bit-Schlüssel, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e659-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="0e659-117">2</span><span class="sxs-lookup"><span data-stu-id="0e659-117">2</span></span>         |
| <span data-ttu-id="0e659-118">**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 128 \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="0e659-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="0e659-119">Verwendet 128-Bit-Schlüssel, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e659-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="0e659-120">3</span><span class="sxs-lookup"><span data-stu-id="0e659-120">3</span></span>         |
| <span data-ttu-id="0e659-121">**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 192 \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="0e659-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="0e659-122">Verwendet 192-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0e659-122">Uses 192-bit keys.</span></span> <span data-ttu-id="0e659-123">Diese Schlüssellänge ist nur für AES verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e659-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="0e659-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="0e659-124">4 // v2.0</span></span> |
| <span data-ttu-id="0e659-125">**CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge \_ 256 \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="0e659-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="0e659-126">Verwendet 256-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0e659-126">Uses 256-bit keys.</span></span> <span data-ttu-id="0e659-127">Diese Schlüssellänge ist nur für AES verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e659-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="0e659-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="0e659-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="0e659-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e659-129">Remarks</span></span>

<span data-ttu-id="0e659-130">Der Enumerationstyp " **CAPICOM- \_ Verschlüsselungs \_ Schlüssel \_ Länge** " wird von der Eigenschaft " [**Algorithmus. keylength**](algorithm-keylength.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e659-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e659-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e659-131">Requirements</span></span>



| <span data-ttu-id="0e659-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e659-132">Requirement</span></span> | <span data-ttu-id="0e659-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0e659-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e659-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0e659-134">Redistributable</span></span><br/> | <span data-ttu-id="0e659-135">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e659-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0e659-136">Header</span><span class="sxs-lookup"><span data-stu-id="0e659-136">Header</span></span><br/>          | <dl> <span data-ttu-id="0e659-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e659-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
