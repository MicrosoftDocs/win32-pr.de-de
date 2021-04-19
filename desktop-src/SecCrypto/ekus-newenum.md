---
description: Die \_ Eigenschaft "netwenum" von EKUs Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: c7d038c0-416f-47f7-94ba-74ca877da7ba
title: EKUs._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72605e0ad7bbb8671ff9a5885a79f1d7836c6efb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355871"
---
# <a name="ekus_newenum-property"></a><span data-ttu-id="ed7d6-104">EKUs. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="ed7d6-104">EKUs.\_NewEnum property</span></span>

<span data-ttu-id="ed7d6-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed7d6-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ed7d6-106">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="ed7d6-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ed7d6-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed7d6-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="ed7d6-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ed7d6-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7d6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7d6-109">Syntax</span></span>


```VB
EKUs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="ed7d6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ed7d6-110">Property value</span></span>

<span data-ttu-id="ed7d6-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed7d6-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed7d6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed7d6-112">Remarks</span></span>

<span data-ttu-id="ed7d6-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed7d6-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7d6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed7d6-114">Requirements</span></span>



| <span data-ttu-id="ed7d6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed7d6-115">Requirement</span></span> | <span data-ttu-id="ed7d6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ed7d6-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7d6-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ed7d6-117">End of client support</span></span><br/> | <span data-ttu-id="ed7d6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed7d6-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed7d6-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ed7d6-119">End of server support</span></span><br/> | <span data-ttu-id="ed7d6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed7d6-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed7d6-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ed7d6-121">Redistributable</span></span><br/>       | <span data-ttu-id="ed7d6-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed7d6-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ed7d6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ed7d6-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ed7d6-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d6-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed7d6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed7d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7d6-126">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="ed7d6-126">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
