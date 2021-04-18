---
description: Fügt der Auflistung ein Attribut Objekt hinzu.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Attribute. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352121"
---
# <a name="attributesadd-method"></a><span data-ttu-id="c5d9e-103">Attribute. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="c5d9e-103">Attributes.Add method</span></span>

<span data-ttu-id="c5d9e-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="c5d9e-105">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c5d9e-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="c5d9e-106">Die **Add** -Methode fügt der Auflistung ein [**Attribut**](attribute.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d9e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d9e-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="c5d9e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5d9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d9e-109">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d9e-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d9e-110">Das [**Attribut**](attribute.md) Objekt, das am Ende der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d9e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5d9e-111">Return value</span></span>

<span data-ttu-id="c5d9e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-112">This method does not return a value.</span></span> <span data-ttu-id="c5d9e-113">Eine Anwendung, die diese Methode verwendet, muss Code enthalten, um eine Ausnahme zu behandeln, die von dieser Methode ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="c5d9e-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d9e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5d9e-114">Requirements</span></span>



| <span data-ttu-id="c5d9e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5d9e-115">Requirement</span></span> | <span data-ttu-id="c5d9e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d9e-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d9e-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c5d9e-117">End of client support</span></span><br/> | <span data-ttu-id="c5d9e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5d9e-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c5d9e-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c5d9e-119">End of server support</span></span><br/> | <span data-ttu-id="c5d9e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5d9e-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c5d9e-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c5d9e-121">Redistributable</span></span><br/>       | <span data-ttu-id="c5d9e-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5d9e-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5d9e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c5d9e-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c5d9e-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5d9e-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d9e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d9e-126">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="c5d9e-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c5d9e-127">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c5d9e-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
