---
description: Ruft die Hash Daten nach erfolgreichen Aufrufen der Hash Methode ab.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData. Value (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373652"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="f0770-103">HashedData. Value (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f0770-103">HashedData.Value property</span></span>

<span data-ttu-id="f0770-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0770-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f0770-105">Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f0770-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f0770-106">Die **value** -Eigenschaft ruft die Hash Daten nach erfolgreichen Aufrufen der [**Hash**](hasheddata-hash.md) Methode ab.</span><span class="sxs-lookup"><span data-stu-id="f0770-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="f0770-107">Der Hashwert wird im Hexadezimal Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0770-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="f0770-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f0770-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0770-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0770-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="f0770-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f0770-110">Property value</span></span>

<span data-ttu-id="f0770-111">Eine Zeichenfolge, die die Hash Daten im Hexadezimal Format enthält.</span><span class="sxs-lookup"><span data-stu-id="f0770-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0770-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0770-112">Remarks</span></span>

<span data-ttu-id="f0770-113">Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die [**Hash**](hasheddata-hash.md) Methode für jedes Datenelement auf.</span><span class="sxs-lookup"><span data-stu-id="f0770-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="f0770-114">Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der **value** -Eigenschaft verkettet.</span><span class="sxs-lookup"><span data-stu-id="f0770-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="f0770-115">Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="f0770-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0770-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0770-116">Requirements</span></span>



| <span data-ttu-id="f0770-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0770-117">Requirement</span></span> | <span data-ttu-id="f0770-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f0770-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0770-119">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f0770-119">End of client support</span></span><br/> | <span data-ttu-id="f0770-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0770-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f0770-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f0770-121">End of server support</span></span><br/> | <span data-ttu-id="f0770-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0770-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f0770-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f0770-123">Redistributable</span></span><br/>       | <span data-ttu-id="f0770-124">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0770-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f0770-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0770-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f0770-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0770-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0770-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0770-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0770-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="f0770-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
