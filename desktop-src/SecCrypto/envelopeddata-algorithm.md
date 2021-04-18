---
description: Ruft den Verschlüsselungsalgorithmus und die Schlüssellänge ab.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData. algorithmuseigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352980"
---
# <a name="envelopeddataalgorithm-property"></a><span data-ttu-id="3feaf-103">EnvelopedData. algorithmuseigenschaft</span><span class="sxs-lookup"><span data-stu-id="3feaf-103">EnvelopedData.Algorithm property</span></span>

<span data-ttu-id="3feaf-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3feaf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3feaf-105">Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="3feaf-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3feaf-106">Die  algorithmuseigenschaft Ruft den Verschlüsselungsalgorithmus und die [*Schlüssellänge*](../secgloss/k-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="3feaf-106">The **Algorithm** property retrieves the encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3feaf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3feaf-107">Syntax</span></span>


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="3feaf-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3feaf-108">Property value</span></span>

<span data-ttu-id="3feaf-109">Ein [**Algorithmusobjekt**](algorithm.md) , das den Verschlüsselungsalgorithmus und die Schlüssellänge enthält.</span><span class="sxs-lookup"><span data-stu-id="3feaf-109">An [**Algorithm**](algorithm.md) object that contains the encryption algorithm and key length.</span></span>

## <a name="requirements"></a><span data-ttu-id="3feaf-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3feaf-110">Requirements</span></span>



| <span data-ttu-id="3feaf-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3feaf-111">Requirement</span></span> | <span data-ttu-id="3feaf-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3feaf-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3feaf-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3feaf-113">End of client support</span></span><br/> | <span data-ttu-id="3feaf-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3feaf-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3feaf-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3feaf-115">End of server support</span></span><br/> | <span data-ttu-id="3feaf-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3feaf-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3feaf-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3feaf-117">Redistributable</span></span><br/>       | <span data-ttu-id="3feaf-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3feaf-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3feaf-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3feaf-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3feaf-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3feaf-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3feaf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3feaf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3feaf-122">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="3feaf-122">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
