---
description: Entfernt ein indiziertes Attribut Objekt aus der Auflistung.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributs. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366785"
---
# <a name="attributesremove-method"></a><span data-ttu-id="c5aa0-103">Attributs. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="c5aa0-103">Attributes.Remove method</span></span>

<span data-ttu-id="c5aa0-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="c5aa0-105">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c5aa0-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c5aa0-106">Die **Remove** -Methode entfernt ein indiziertes [**Attribut**](attribute.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5aa0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5aa0-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="c5aa0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5aa0-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5aa0-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5aa0-110">Der Index des [**Attribut**](attribute.md) Objekts, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5aa0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5aa0-111">Return value</span></span>

<span data-ttu-id="c5aa0-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5aa0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5aa0-113">Remarks</span></span>

<span data-ttu-id="c5aa0-114">Anwendungen, die diese Methode verwenden, müssen Code enthalten, um eine Ausnahme zu behandeln, die von dieser Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5aa0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5aa0-115">Requirements</span></span>



| <span data-ttu-id="c5aa0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5aa0-116">Requirement</span></span> | <span data-ttu-id="c5aa0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c5aa0-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5aa0-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c5aa0-118">End of client support</span></span><br/> | <span data-ttu-id="c5aa0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5aa0-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c5aa0-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c5aa0-120">End of server support</span></span><br/> | <span data-ttu-id="c5aa0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5aa0-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c5aa0-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c5aa0-122">Redistributable</span></span><br/>       | <span data-ttu-id="c5aa0-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5aa0-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5aa0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c5aa0-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c5aa0-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5aa0-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5aa0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5aa0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5aa0-127">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="c5aa0-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c5aa0-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c5aa0-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
