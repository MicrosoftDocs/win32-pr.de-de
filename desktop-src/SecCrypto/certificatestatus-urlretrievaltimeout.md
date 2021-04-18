---
description: Legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus. UrlRetrievalTimeout-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365376"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="655f5-103">CertificateStatus. UrlRetrievalTimeout-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="655f5-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="655f5-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="655f5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="655f5-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="655f5-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="655f5-106">Die **UrlRetrievalTimeout** -Eigenschaft legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="655f5-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="655f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="655f5-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="655f5-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="655f5-108">Property value</span></span>

<span data-ttu-id="655f5-109">Die Anzahl der Sekunden, bevor eine URL als nicht erreichbar festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="655f5-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="655f5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="655f5-110">Remarks</span></span>

<span data-ttu-id="655f5-111">Wenn diese Eigenschaft nicht festgelegt ist, beträgt das Standard Timeout 15 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="655f5-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="655f5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="655f5-112">Requirements</span></span>



| <span data-ttu-id="655f5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="655f5-113">Requirement</span></span> | <span data-ttu-id="655f5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="655f5-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="655f5-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="655f5-115">End of client support</span></span><br/> | <span data-ttu-id="655f5-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="655f5-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="655f5-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="655f5-117">End of server support</span></span><br/> | <span data-ttu-id="655f5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="655f5-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="655f5-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="655f5-119">Redistributable</span></span><br/>       | <span data-ttu-id="655f5-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="655f5-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="655f5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="655f5-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="655f5-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="655f5-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
