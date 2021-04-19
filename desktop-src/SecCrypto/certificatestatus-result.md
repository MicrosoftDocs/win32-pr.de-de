---
description: Die Result-Eigenschaft ruft einen Wert ab, der angibt, ob das Zertifikat gültig ist. Dies ist die Standard Eigenschaft.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352016"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="6db91-104">CertificateStatus. Result (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6db91-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="6db91-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6db91-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6db91-106">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="6db91-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6db91-107">Die **Result** -Eigenschaft ruft einen Wert ab, der angibt, ob das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6db91-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="6db91-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6db91-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db91-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6db91-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6db91-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6db91-110">Property value</span></span>

<span data-ttu-id="6db91-111">**True** gibt an, dass das Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6db91-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="6db91-112">Die Gültigkeit des Zertifikats wird mithilfe der aktuellen Einstellung der [**checkflag**](certificatestatus-checkflag.md) -Eigenschaft und der verschiedenen Richtlinien Einstellungen überprüft.</span><span class="sxs-lookup"><span data-stu-id="6db91-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db91-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6db91-113">Requirements</span></span>



| <span data-ttu-id="6db91-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6db91-114">Requirement</span></span> | <span data-ttu-id="6db91-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6db91-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6db91-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6db91-116">End of client support</span></span><br/> | <span data-ttu-id="6db91-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6db91-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6db91-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6db91-118">End of server support</span></span><br/> | <span data-ttu-id="6db91-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6db91-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6db91-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6db91-120">Redistributable</span></span><br/>       | <span data-ttu-id="6db91-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6db91-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6db91-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6db91-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6db91-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6db91-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
