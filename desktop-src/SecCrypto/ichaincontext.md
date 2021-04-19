---
description: Bietet Zugriff auf den Kontext eines CAPICOM-Ketten Objekts. In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Ichaincontext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361266"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="44da3-104">Ichaincontext-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="44da3-104">IChainContext interface</span></span>

<span data-ttu-id="44da3-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="44da3-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="44da3-106">Die **ichaincontext** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM- [**Ketten**](chain.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="44da3-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="44da3-107">In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44da3-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="44da3-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="44da3-108">When to use</span></span>

<span data-ttu-id="44da3-109">Verwenden Sie diese Schnittstelle, wenn Sie in einer anderen Ableitung von CryptoAPI ein CAPICOM- [**Ketten**](chain.md) Objekt verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="44da3-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="44da3-110">Member</span><span class="sxs-lookup"><span data-stu-id="44da3-110">Members</span></span>

<span data-ttu-id="44da3-111">Die **ichaincontext** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44da3-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="44da3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="44da3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="44da3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44da3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="44da3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="44da3-114">Methods</span></span>

<span data-ttu-id="44da3-115">Die **ichaincontext** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="44da3-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="44da3-116">Methode</span><span class="sxs-lookup"><span data-stu-id="44da3-116">Method</span></span>                                           | <span data-ttu-id="44da3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44da3-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44da3-118">**Freecontext**</span><span class="sxs-lookup"><span data-stu-id="44da3-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="44da3-119">Gibt einen pccert- \_ Ketten kontextfrei, \_ der über die [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="44da3-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="44da3-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44da3-120">Properties</span></span>

<span data-ttu-id="44da3-121">Die **ichaincontext** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44da3-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="44da3-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44da3-122">Property</span></span>                                                      | <span data-ttu-id="44da3-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="44da3-123">Access type</span></span>           | <span data-ttu-id="44da3-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44da3-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="44da3-125">**ChainContext**</span><span class="sxs-lookup"><span data-stu-id="44da3-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="44da3-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="44da3-126">Read/write</span></span><br/> | <span data-ttu-id="44da3-127">Legt den pccert- \_ Ketten Kontext eines Zertifikats fest oder ruft ihn ab \_ .</span><span class="sxs-lookup"><span data-stu-id="44da3-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="44da3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44da3-128">Requirements</span></span>



| <span data-ttu-id="44da3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44da3-129">Requirement</span></span> | <span data-ttu-id="44da3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="44da3-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44da3-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="44da3-131">Redistributable</span></span><br/> | <span data-ttu-id="44da3-132">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="44da3-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44da3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="44da3-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="44da3-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44da3-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




