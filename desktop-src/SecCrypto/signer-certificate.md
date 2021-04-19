---
description: Legt das Zertifikat Objekt fest, das das Zertifikat eines Signatur Gebers der Daten darstellt, oder ruft es ab.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Signer. Certificate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367438"
---
# <a name="signercertificate-property"></a><span data-ttu-id="7d276-103">Signer. Certificate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7d276-103">Signer.Certificate property</span></span>

<span data-ttu-id="7d276-104">\[Die **Zertifikat** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7d276-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d276-105">Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="7d276-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7d276-106">Die **Certificate** -Eigenschaft legt das [**Zertifikat**](certificate.md) Objekt fest oder ruft es ab, das das Zertifikat eines Signatur Gebers für die Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d276-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="7d276-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7d276-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d276-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d276-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="7d276-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7d276-109">Property value</span></span>

<span data-ttu-id="7d276-110">Das [**Zertifikat**](certificate.md) Objekt, das das Zertifikat eines Signatur Gebers der Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d276-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d276-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d276-111">Remarks</span></span>

<span data-ttu-id="7d276-112">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7d276-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d276-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d276-113">Requirements</span></span>



| <span data-ttu-id="7d276-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d276-114">Requirement</span></span> | <span data-ttu-id="7d276-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7d276-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d276-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7d276-116">Redistributable</span></span><br/> | <span data-ttu-id="7d276-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d276-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d276-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7d276-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="7d276-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d276-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d276-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d276-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d276-121">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="7d276-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
