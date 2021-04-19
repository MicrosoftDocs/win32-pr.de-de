---
description: Die Oid-Eigenschaft ruft den Objekt Bezeichner für die Erweiterung ab. Dies ist die Standard Eigenschaft.
ms.assetid: 51efd413-f9f0-4577-a554-de6afc32dd87
title: Extension. Oid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9bf52fc8c2381837a21cd87115626552ec1a6e4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373696"
---
# <a name="extensionoid-property"></a><span data-ttu-id="94266-104">Extension. Oid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="94266-104">Extension.OID property</span></span>

<span data-ttu-id="94266-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="94266-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="94266-106">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="94266-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="94266-107">Die **OID** -Eigenschaft ruft den Objekt Bezeichner für die Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="94266-107">The **OID** property retrieves the object identifier for the extension.</span></span> <span data-ttu-id="94266-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="94266-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="94266-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="94266-109">Syntax</span></span>


```VB
Extension.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="94266-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="94266-110">Property value</span></span>

<span data-ttu-id="94266-111">Ein [**OID**](oid.md) -Objekt, das den Objekt Bezeichner der Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="94266-111">An [**OID**](oid.md) object that represents the object identifier of the extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="94266-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94266-112">Requirements</span></span>



| <span data-ttu-id="94266-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94266-113">Requirement</span></span> | <span data-ttu-id="94266-114">Wert</span><span class="sxs-lookup"><span data-stu-id="94266-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94266-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="94266-115">End of client support</span></span><br/> | <span data-ttu-id="94266-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94266-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="94266-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="94266-117">End of server support</span></span><br/> | <span data-ttu-id="94266-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94266-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="94266-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="94266-119">Redistributable</span></span><br/>       | <span data-ttu-id="94266-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="94266-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="94266-121">DLL</span><span class="sxs-lookup"><span data-stu-id="94266-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="94266-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94266-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
