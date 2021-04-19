---
description: Die algorithmuseigenschaft Ruft das Oid-Objekt ab, das den Algorithmus identifiziert, der vom öffentlichen Schlüssel verwendet wird. Dies ist die Standard Eigenschaft.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. algorithmuseigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366742"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="08b09-104">PublicKey. algorithmuseigenschaft</span><span class="sxs-lookup"><span data-stu-id="08b09-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="08b09-105">\[Die **algorithmuseigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="08b09-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08b09-106">Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="08b09-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="08b09-107">Die  algorithmuseigenschaft Ruft das [**OID**](oid.md) -Objekt ab, das den Algorithmus identifiziert, der vom öffentlichen Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08b09-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="08b09-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08b09-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b09-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b09-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="08b09-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="08b09-110">Property value</span></span>

<span data-ttu-id="08b09-111">Das [**OID**](oid.md) -Objekt, das den vom öffentlichen Schlüssel verwendeten Algorithmus identifiziert.</span><span class="sxs-lookup"><span data-stu-id="08b09-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b09-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08b09-112">Requirements</span></span>



| <span data-ttu-id="08b09-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08b09-113">Requirement</span></span> | <span data-ttu-id="08b09-114">Wert</span><span class="sxs-lookup"><span data-stu-id="08b09-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b09-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08b09-115">Redistributable</span></span><br/> | <span data-ttu-id="08b09-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="08b09-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08b09-117">DLL</span><span class="sxs-lookup"><span data-stu-id="08b09-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="08b09-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b09-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b09-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b09-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b09-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="08b09-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
