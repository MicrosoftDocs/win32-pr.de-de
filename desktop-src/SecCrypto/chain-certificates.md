---
description: Die Eigenschaft Zertifikate Ruft eine Zertifikat Sammlung ab, die die Zertifikate in der Kette darstellt. Dies ist die Standard Eigenschaft.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2:: Zertifikats (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366030"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="385d4-104">IChain2:: Zertifikats (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="385d4-104">IChain2::Certificates property</span></span>

<span data-ttu-id="385d4-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="385d4-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="385d4-106">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="385d4-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="385d4-107">Die Eigenschaft **Zertifikate** Ruft eine [**Zertifikat**](certificates.md) Sammlung ab, die die Zertifikate in der Kette darstellt.</span><span class="sxs-lookup"><span data-stu-id="385d4-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="385d4-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="385d4-108">This is the default property.</span></span>

<span data-ttu-id="385d4-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="385d4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="385d4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="385d4-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="385d4-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="385d4-111">Property value</span></span>

<span data-ttu-id="385d4-112">Eine [**Zertifikat**](certificates.md) Sammlung, die zum Abrufen von Informationen zu jedem Zertifikat in der Kette verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="385d4-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="385d4-113">Das erste Zertifikat in der zurückgegebenen Auflistung, "Certificate **. Item**(1)", ist das Endzertifikat der Kette.</span><span class="sxs-lookup"><span data-stu-id="385d4-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="385d4-114">Das letzte Zertifikat in der Sammlung, "Certificate **. Item**" ("**Zertifikate. count**"), ist das Stamm [*Zertifikat*](../secgloss/r-gly.md) der Kette.</span><span class="sxs-lookup"><span data-stu-id="385d4-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="385d4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="385d4-115">Requirements</span></span>



| <span data-ttu-id="385d4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="385d4-116">Requirement</span></span> | <span data-ttu-id="385d4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="385d4-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="385d4-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="385d4-118">End of client support</span></span><br/> | <span data-ttu-id="385d4-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="385d4-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="385d4-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="385d4-120">End of server support</span></span><br/> | <span data-ttu-id="385d4-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="385d4-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="385d4-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="385d4-122">Redistributable</span></span><br/>       | <span data-ttu-id="385d4-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="385d4-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="385d4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="385d4-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="385d4-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="385d4-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
