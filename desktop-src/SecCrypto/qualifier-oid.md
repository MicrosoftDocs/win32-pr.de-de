---
description: Ruft die Objekt-ID des Qualifizierers ab.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Qualifizierer. Oid-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370743"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="b7430-103">Qualifizierer. Oid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7430-103">Qualifier.OID property</span></span>

<span data-ttu-id="b7430-104">\[Die **OID** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b7430-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b7430-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]</span><span class="sxs-lookup"><span data-stu-id="b7430-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="b7430-106">Die **OID** -Eigenschaft ruft die Objekt-ID des Qualifizierers ab.</span><span class="sxs-lookup"><span data-stu-id="b7430-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="b7430-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7430-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7430-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7430-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="b7430-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7430-109">Property value</span></span>

<span data-ttu-id="b7430-110">Ein [**OID**](oid.md) -Objekt, das den Qualifizierer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b7430-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7430-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7430-111">Requirements</span></span>



| <span data-ttu-id="b7430-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7430-112">Requirement</span></span> | <span data-ttu-id="b7430-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b7430-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7430-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b7430-114">Redistributable</span></span><br/> | <span data-ttu-id="b7430-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7430-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7430-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b7430-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="b7430-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7430-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7430-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7430-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7430-119">**Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="b7430-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
