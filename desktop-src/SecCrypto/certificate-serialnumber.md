---
description: Ruft eine Zeichenfolge ab, die die Seriennummer des Zertifikats enthält.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Certificate. SerialNumber (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367649"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="ee6f9-103">Certificate. SerialNumber (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee6f9-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="ee6f9-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ee6f9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ee6f9-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ee6f9-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ee6f9-106">Die **serialNumber** -Eigenschaft ruft eine Zeichenfolge ab, die die Seriennummer des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="ee6f9-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="ee6f9-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ee6f9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee6f9-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="ee6f9-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ee6f9-109">Property value</span></span>

<span data-ttu-id="ee6f9-110">Eine Zeichenfolge, die die Seriennummer des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="ee6f9-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee6f9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee6f9-111">Requirements</span></span>



| <span data-ttu-id="ee6f9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee6f9-112">Requirement</span></span> | <span data-ttu-id="ee6f9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ee6f9-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6f9-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ee6f9-114">End of client support</span></span><br/> | <span data-ttu-id="ee6f9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee6f9-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ee6f9-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ee6f9-116">End of server support</span></span><br/> | <span data-ttu-id="ee6f9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee6f9-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ee6f9-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ee6f9-118">Redistributable</span></span><br/>       | <span data-ttu-id="ee6f9-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee6f9-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ee6f9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ee6f9-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ee6f9-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee6f9-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
