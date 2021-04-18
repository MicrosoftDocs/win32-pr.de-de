---
description: Löscht alle Attribut Objekte aus der Auflistung.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Attribute. Clear-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365539"
---
# <a name="attributesclear-method"></a><span data-ttu-id="8e837-103">Attribute. Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="8e837-103">Attributes.Clear method</span></span>

<span data-ttu-id="8e837-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8e837-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="8e837-105">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8e837-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="8e837-106">Die **Clear** -Methode löscht alle [**Attribut**](attribute.md) Objekte aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8e837-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e837-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e837-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="8e837-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e837-108">Parameters</span></span>

<span data-ttu-id="8e837-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8e837-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e837-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e837-110">Return value</span></span>

<span data-ttu-id="8e837-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8e837-111">This method does not return a value.</span></span> <span data-ttu-id="8e837-112">Eine Anwendung, die diese Methode verwendet, muss Code enthalten, um eine Ausnahme zu behandeln, die von dieser Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8e837-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e837-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e837-113">Requirements</span></span>



| <span data-ttu-id="8e837-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e837-114">Requirement</span></span> | <span data-ttu-id="8e837-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8e837-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e837-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8e837-116">End of client support</span></span><br/> | <span data-ttu-id="8e837-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e837-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8e837-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8e837-118">End of server support</span></span><br/> | <span data-ttu-id="8e837-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e837-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8e837-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8e837-120">Redistributable</span></span><br/>       | <span data-ttu-id="8e837-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e837-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8e837-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8e837-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8e837-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e837-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e837-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e837-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e837-125">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="8e837-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="8e837-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8e837-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
