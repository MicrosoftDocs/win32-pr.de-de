---
description: Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Erweiterung. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356401"
---
# <a name="extensioniscritical-property"></a><span data-ttu-id="ffe83-103">Erweiterung. IsCritical (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ffe83-103">Extension.IsCritical property</span></span>

<span data-ttu-id="ffe83-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffe83-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ffe83-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ffe83-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ffe83-106">Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffe83-106">The **IsCritical** property retrieves a Boolean value that indicates whether the extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe83-107">Syntax</span></span>


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ffe83-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ffe83-108">Property value</span></span>

<span data-ttu-id="ffe83-109">**True** gibt an, dass die Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ffe83-109">If **true**, the extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe83-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffe83-110">Requirements</span></span>



| <span data-ttu-id="ffe83-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffe83-111">Requirement</span></span> | <span data-ttu-id="ffe83-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe83-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe83-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ffe83-113">End of client support</span></span><br/> | <span data-ttu-id="ffe83-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffe83-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ffe83-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ffe83-115">End of server support</span></span><br/> | <span data-ttu-id="ffe83-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffe83-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ffe83-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ffe83-117">Redistributable</span></span><br/>       | <span data-ttu-id="ffe83-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ffe83-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ffe83-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ffe83-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ffe83-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffe83-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
