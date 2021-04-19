---
description: Ruft eine Zeichenfolge ab, die den Namen des Zertifikat Ausstellers enthält.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Certificate. IssuerName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370087"
---
# <a name="certificateissuername-property"></a><span data-ttu-id="b1fb4-103">Certificate. IssuerName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1fb4-103">Certificate.IssuerName property</span></span>

<span data-ttu-id="b1fb4-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1fb4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b1fb4-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="b1fb4-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b1fb4-106">Die **IssuerName** -Eigenschaft ruft eine Zeichenfolge ab, die den Namen des Zertifikat Ausstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="b1fb4-106">The **IssuerName** property retrieves a string that contains the name of the certificate issuer.</span></span>

<span data-ttu-id="b1fb4-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b1fb4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1fb4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1fb4-108">Syntax</span></span>


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a><span data-ttu-id="b1fb4-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b1fb4-109">Property value</span></span>

<span data-ttu-id="b1fb4-110">Eine Zeichenfolge, die den Namen des Zertifikat Ausstellers enthält.</span><span class="sxs-lookup"><span data-stu-id="b1fb4-110">String that contains the name of the certificate issuer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1fb4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1fb4-111">Requirements</span></span>



| <span data-ttu-id="b1fb4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1fb4-112">Requirement</span></span> | <span data-ttu-id="b1fb4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b1fb4-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fb4-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b1fb4-114">End of client support</span></span><br/> | <span data-ttu-id="b1fb4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1fb4-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b1fb4-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b1fb4-116">End of server support</span></span><br/> | <span data-ttu-id="b1fb4-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1fb4-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b1fb4-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b1fb4-118">Redistributable</span></span><br/>       | <span data-ttu-id="b1fb4-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1fb4-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b1fb4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b1fb4-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b1fb4-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1fb4-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
