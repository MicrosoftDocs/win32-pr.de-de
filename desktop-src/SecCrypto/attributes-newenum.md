---
description: Die \_ Eigenschaft "netwenum" von Attributen Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Attributes._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361964"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="7b343-104">Attribute. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="7b343-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="7b343-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b343-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7b343-106">Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="7b343-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7b343-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b343-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="7b343-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7b343-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b343-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b343-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="7b343-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7b343-110">Property value</span></span>

<span data-ttu-id="7b343-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b343-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b343-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b343-112">Remarks</span></span>

<span data-ttu-id="7b343-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b343-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b343-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b343-114">Requirements</span></span>



| <span data-ttu-id="7b343-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b343-115">Requirement</span></span> | <span data-ttu-id="7b343-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7b343-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b343-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7b343-117">End of client support</span></span><br/> | <span data-ttu-id="7b343-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b343-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b343-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7b343-119">End of server support</span></span><br/> | <span data-ttu-id="7b343-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b343-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b343-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7b343-121">Redistributable</span></span><br/>       | <span data-ttu-id="7b343-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b343-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b343-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7b343-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7b343-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b343-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b343-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b343-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b343-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7b343-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
