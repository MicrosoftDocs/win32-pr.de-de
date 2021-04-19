---
description: Ruft die Anzahl der Attribut Objekte in der Auflistung ab.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attribute. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361542"
---
# <a name="attributescount-property"></a><span data-ttu-id="28039-103">Attribute. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28039-103">Attributes.Count property</span></span>

<span data-ttu-id="28039-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28039-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="28039-105">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="28039-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="28039-106">Die **count** -Eigenschaft ruft die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="28039-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="28039-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="28039-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28039-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28039-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="28039-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="28039-109">Property value</span></span>

<span data-ttu-id="28039-110">Die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="28039-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="28039-111">Jedes **Attribut** Objekt stellt ein einzelnes Attribut in der Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="28039-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="28039-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28039-112">Remarks</span></span>

<span data-ttu-id="28039-113">Die **count** -Eigenschaft kann verwendet werden, um das letzte [**Attribut**](attribute.md) Objekt in der Auflistung anzugeben, wenn ein bestimmtes **Attribut** Objekt mithilfe der [**Attribute. Item**](attributes-item.md) -Eigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="28039-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="28039-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28039-114">Requirements</span></span>



| <span data-ttu-id="28039-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28039-115">Requirement</span></span> | <span data-ttu-id="28039-116">Wert</span><span class="sxs-lookup"><span data-stu-id="28039-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28039-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="28039-117">End of client support</span></span><br/> | <span data-ttu-id="28039-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28039-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="28039-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="28039-119">End of server support</span></span><br/> | <span data-ttu-id="28039-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28039-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="28039-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="28039-121">Redistributable</span></span><br/>       | <span data-ttu-id="28039-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="28039-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="28039-123">DLL</span><span class="sxs-lookup"><span data-stu-id="28039-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="28039-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28039-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28039-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28039-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28039-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="28039-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
