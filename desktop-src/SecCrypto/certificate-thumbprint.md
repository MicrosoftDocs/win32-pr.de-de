---
description: Ruft eine hexadezimale Zeichenfolge ab, die den SHA-1-Hash des Zertifikats enthält.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Certificate. Thumbprint-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364806"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="e396f-103">Certificate. Thumbprint-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e396f-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="e396f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e396f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e396f-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e396f-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e396f-106">Die **Thumbprint** -Eigenschaft ruft eine hexadezimale Zeichenfolge ab, die den [*SHA-1-*](../secgloss/s-gly.md) Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="e396f-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="e396f-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e396f-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e396f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e396f-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="e396f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e396f-109">Property value</span></span>

<span data-ttu-id="e396f-110">Eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="e396f-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e396f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e396f-111">Requirements</span></span>



| <span data-ttu-id="e396f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e396f-112">Requirement</span></span> | <span data-ttu-id="e396f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e396f-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e396f-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e396f-114">End of client support</span></span><br/> | <span data-ttu-id="e396f-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e396f-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e396f-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e396f-116">End of server support</span></span><br/> | <span data-ttu-id="e396f-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e396f-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e396f-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e396f-118">Redistributable</span></span><br/>       | <span data-ttu-id="e396f-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e396f-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e396f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e396f-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e396f-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e396f-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e396f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e396f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e396f-123">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="e396f-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
