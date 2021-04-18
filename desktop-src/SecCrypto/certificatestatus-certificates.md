---
description: Legt die Auflistung der Zertifikate fest, die zum Erstellen der Zertifikat Kette verwendet werden können, oder ruft diese ab.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: CertificateStatus. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372293"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="0303d-103">CertificateStatus. Zertifikats (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0303d-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="0303d-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0303d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0303d-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0303d-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0303d-106">Mit der Eigenschaft **Zertifikate** wird die Sammlung von Zertifikaten festgelegt oder abgerufen, die zum Erstellen der Zertifikat Kette verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0303d-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="0303d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0303d-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="0303d-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0303d-108">Property value</span></span>

<span data-ttu-id="0303d-109">Ein [**Zertifikate**](certificates.md) -Objekt, das die Sammlung von Zertifikaten darstellt, die zum Erstellen der Zertifikat Kette verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0303d-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="0303d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0303d-110">Requirements</span></span>



| <span data-ttu-id="0303d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0303d-111">Requirement</span></span> | <span data-ttu-id="0303d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0303d-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0303d-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0303d-113">End of client support</span></span><br/> | <span data-ttu-id="0303d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0303d-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0303d-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0303d-115">End of server support</span></span><br/> | <span data-ttu-id="0303d-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0303d-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0303d-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0303d-117">Redistributable</span></span><br/>       | <span data-ttu-id="0303d-118">CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0303d-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0303d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0303d-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0303d-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0303d-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
