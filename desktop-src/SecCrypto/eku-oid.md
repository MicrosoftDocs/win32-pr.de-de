---
description: Legt eine Zeichenfolge fest oder ruft eine Zeichenfolge ab, die einen EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Ieku:: OID (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370222"
---
# <a name="iekuoid-property"></a><span data-ttu-id="59d2b-103">Ieku:: OID (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="59d2b-103">IEKU::OID property</span></span>

<span data-ttu-id="59d2b-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59d2b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="59d2b-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="59d2b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="59d2b-106">Die **OID** -Eigenschaft legt eine Zeichenfolge fest oder ruft Sie ab, die einen EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h definiert.</span><span class="sxs-lookup"><span data-stu-id="59d2b-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="59d2b-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="59d2b-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59d2b-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="59d2b-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="59d2b-109">Property value</span></span>

<span data-ttu-id="59d2b-110">Eine Zeichenfolge, die den EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h definiert.</span><span class="sxs-lookup"><span data-stu-id="59d2b-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d2b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59d2b-111">Remarks</span></span>

<span data-ttu-id="59d2b-112">Diese Eigenschaft verwendet nicht das in CAPICOM 2,0 eingeführte [**OID**](oid.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="59d2b-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d2b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59d2b-113">Requirements</span></span>



| <span data-ttu-id="59d2b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59d2b-114">Requirement</span></span> | <span data-ttu-id="59d2b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="59d2b-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59d2b-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="59d2b-116">End of client support</span></span><br/> | <span data-ttu-id="59d2b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59d2b-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="59d2b-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="59d2b-118">End of server support</span></span><br/> | <span data-ttu-id="59d2b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59d2b-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="59d2b-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="59d2b-120">Redistributable</span></span><br/>       | <span data-ttu-id="59d2b-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="59d2b-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="59d2b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="59d2b-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="59d2b-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59d2b-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
