---
description: Legt einen booleschen Wert fest, der angibt, ob das Zertifikat archiviert ist, oder ruft diesen ab.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate. archiviert (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372006"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="dbba9-103">Certificate. archiviert (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dbba9-103">Certificate.Archived property</span></span>

<span data-ttu-id="dbba9-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbba9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="dbba9-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="dbba9-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="dbba9-106">Die **Archivierte** Eigenschaft legt einen booleschen Wert fest oder ruft ihn ab, der angibt, ob das Zertifikat archiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbba9-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="dbba9-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dbba9-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbba9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbba9-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="dbba9-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dbba9-109">Property value</span></span>

<span data-ttu-id="dbba9-110">Ein boolescher Wert, der angibt, ob das Zertifikat archiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbba9-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="dbba9-111">**True** gibt an, dass das Zertifikat archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="dbba9-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="dbba9-112">Beachten Sie, dass das Zertifikat durch Ändern des Werts von **false** in **true** archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="dbba9-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbba9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbba9-113">Remarks</span></span>

<span data-ttu-id="dbba9-114">Diese Eigenschaft löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="dbba9-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="dbba9-115">Ein archiviertes Zertifikat ist auf der Benutzeroberfläche der Zertifikat Verwaltung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="dbba9-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="dbba9-116">Außerdem werden Archivierte Zertifikate nicht in die [**Store. Open**](store-open.md) -Methode eingeschlossen, es sei denn, dass CAPICOM \_ Store \_ Open \_ include \_ archiviert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dbba9-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbba9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbba9-117">Requirements</span></span>



| <span data-ttu-id="dbba9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbba9-118">Requirement</span></span> | <span data-ttu-id="dbba9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dbba9-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbba9-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="dbba9-120">End of client support</span></span><br/> | <span data-ttu-id="dbba9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbba9-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="dbba9-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="dbba9-122">End of server support</span></span><br/> | <span data-ttu-id="dbba9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbba9-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="dbba9-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dbba9-124">Redistributable</span></span><br/>       | <span data-ttu-id="dbba9-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbba9-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dbba9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dbba9-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="dbba9-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
