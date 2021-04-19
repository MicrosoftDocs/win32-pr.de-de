---
description: Ruft die-Auflistung ab, die alle Zertifikate im Speicher enthält.
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: Store. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356459"
---
# <a name="storecertificates-property"></a><span data-ttu-id="039cc-103">Store. Zertifikats (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="039cc-103">Store.Certificates property</span></span>

<span data-ttu-id="039cc-104">\[Die Eigenschaft **Zertifikate** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="039cc-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="039cc-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="039cc-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="039cc-106">Mit der Eigenschaft **Zertifikate** wird die Sammlung abgerufen, die alle Zertifikate im Speicher enthält.</span><span class="sxs-lookup"><span data-stu-id="039cc-106">The **Certificates** property retrieves the collection that includes all of the certificates in the store.</span></span> <span data-ttu-id="039cc-107">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="039cc-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="039cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="039cc-108">Syntax</span></span>


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="039cc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="039cc-109">Property value</span></span>

<span data-ttu-id="039cc-110">Die Sammlung der Zertifikate im Speicher.</span><span class="sxs-lookup"><span data-stu-id="039cc-110">The collection of certificates in the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="039cc-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="039cc-111">Requirements</span></span>



| <span data-ttu-id="039cc-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="039cc-112">Requirement</span></span> | <span data-ttu-id="039cc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="039cc-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="039cc-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="039cc-114">Redistributable</span></span><br/> | <span data-ttu-id="039cc-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="039cc-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="039cc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="039cc-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="039cc-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="039cc-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="039cc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="039cc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039cc-119">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="039cc-119">**Store**</span></span>](store.md)
</dt> </dl>

 

 
