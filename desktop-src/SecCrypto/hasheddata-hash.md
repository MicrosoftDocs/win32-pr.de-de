---
description: Erstellt einen Hash der angegebenen Zeichenfolge.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData. Hash-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359264"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="08a90-103">HashedData. Hash-Methode</span><span class="sxs-lookup"><span data-stu-id="08a90-103">HashedData.Hash method</span></span>

<span data-ttu-id="08a90-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08a90-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="08a90-105">Verwenden Sie stattdessen die [**HashAlgorithm-Klasse**](/previous-versions/windows/) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="08a90-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="08a90-106">Die **Hash** Methode erstellt einen Hash der angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="08a90-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08a90-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="08a90-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08a90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a90-109">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="08a90-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="08a90-110">Eine Zeichenfolge, die den zu Hashwert enthält.</span><span class="sxs-lookup"><span data-stu-id="08a90-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a90-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08a90-111">Return value</span></span>

<span data-ttu-id="08a90-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="08a90-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a90-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08a90-113">Remarks</span></span>

<span data-ttu-id="08a90-114">Um den Hash einer großen Datenmenge zu erstellen, rufen Sie die **Hash** Methode für jedes Datenelement auf.</span><span class="sxs-lookup"><span data-stu-id="08a90-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="08a90-115">Der Hash der einzelnen Daten Daten wird bis zum Lesen der Eigenschaft mit der [**value**](hasheddata-value.md) -Eigenschaft verkettet.</span><span class="sxs-lookup"><span data-stu-id="08a90-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="08a90-116">Der Inhalt der **value** -Eigenschaft wird zurückgesetzt, wenn die Eigenschaft gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="08a90-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a90-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08a90-117">Requirements</span></span>



| <span data-ttu-id="08a90-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08a90-118">Requirement</span></span> | <span data-ttu-id="08a90-119">Wert</span><span class="sxs-lookup"><span data-stu-id="08a90-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a90-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="08a90-120">End of client support</span></span><br/> | <span data-ttu-id="08a90-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08a90-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="08a90-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="08a90-122">End of server support</span></span><br/> | <span data-ttu-id="08a90-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08a90-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="08a90-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08a90-124">Redistributable</span></span><br/>       | <span data-ttu-id="08a90-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="08a90-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08a90-126">DLL</span><span class="sxs-lookup"><span data-stu-id="08a90-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="08a90-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a90-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
