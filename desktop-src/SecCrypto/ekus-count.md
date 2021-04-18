---
description: Ruft die Anzahl der EKU-Objekte in der Auflistung ab.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKUs. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354700"
---
# <a name="ekuscount-property"></a><span data-ttu-id="d2d77-103">EKUs. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2d77-103">EKUs.Count property</span></span>

<span data-ttu-id="d2d77-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2d77-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d2d77-105">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d2d77-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d2d77-106">Die **count** -Eigenschaft ruft die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d2d77-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="d2d77-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d2d77-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d77-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2d77-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="d2d77-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d2d77-109">Property value</span></span>

<span data-ttu-id="d2d77-110">Die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d2d77-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="d2d77-111">Jedes **EKU** -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="d2d77-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d77-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2d77-112">Remarks</span></span>

<span data-ttu-id="d2d77-113">Die **count** -Eigenschaft kann verwendet werden, um das letzte [**EKU**](eku.md) -Objekt in einer Auflistung anzugeben, wenn ein bestimmtes **EKU** -Objekt mithilfe der [**EKUs. Item**](ekus-item.md) -Eigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d2d77-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d77-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2d77-114">Requirements</span></span>



| <span data-ttu-id="d2d77-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2d77-115">Requirement</span></span> | <span data-ttu-id="d2d77-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d2d77-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d77-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d2d77-117">End of client support</span></span><br/> | <span data-ttu-id="d2d77-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2d77-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2d77-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d2d77-119">End of server support</span></span><br/> | <span data-ttu-id="d2d77-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2d77-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2d77-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d2d77-121">Redistributable</span></span><br/>       | <span data-ttu-id="d2d77-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2d77-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2d77-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d77-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2d77-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2d77-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
