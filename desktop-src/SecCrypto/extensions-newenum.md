---
description: Die \_ Eigenschaft "netwenum" der Erweiterungen Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: 0e461683-bb48-4961-91ef-36af1c3f863e
title: Extensions._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5b605241e8173b8a41779fa00b661a9e2f383ac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358013"
---
# <a name="extensions_newenum-property"></a><span data-ttu-id="0097c-104">Erweiterungen. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="0097c-104">Extensions.\_NewEnum property</span></span>

<span data-ttu-id="0097c-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0097c-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0097c-106">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0097c-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0097c-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0097c-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="0097c-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="0097c-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="0097c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0097c-109">Syntax</span></span>


```VB
Extensions._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="0097c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0097c-110">Property value</span></span>

<span data-ttu-id="0097c-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0097c-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0097c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0097c-112">Remarks</span></span>

<span data-ttu-id="0097c-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0097c-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="0097c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0097c-114">Requirements</span></span>



| <span data-ttu-id="0097c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0097c-115">Requirement</span></span> | <span data-ttu-id="0097c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0097c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0097c-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0097c-117">End of client support</span></span><br/> | <span data-ttu-id="0097c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0097c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0097c-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0097c-119">End of server support</span></span><br/> | <span data-ttu-id="0097c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0097c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0097c-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0097c-121">Redistributable</span></span><br/>       | <span data-ttu-id="0097c-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0097c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0097c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0097c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0097c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0097c-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0097c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0097c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0097c-126">**Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="0097c-126">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
