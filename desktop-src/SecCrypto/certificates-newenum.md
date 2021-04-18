---
description: Die \_ Eigenschaft "netwenum" von Zertifikaten Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354801"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="8a6d7-104">Zertifikate. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="8a6d7-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="8a6d7-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8a6d7-106">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8a6d7-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8a6d7-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="8a6d7-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6d7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a6d7-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="8a6d7-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8a6d7-110">Property value</span></span>

<span data-ttu-id="8a6d7-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6d7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a6d7-112">Remarks</span></span>

<span data-ttu-id="8a6d7-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6d7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a6d7-114">Requirements</span></span>



| <span data-ttu-id="8a6d7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a6d7-115">Requirement</span></span> | <span data-ttu-id="8a6d7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8a6d7-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6d7-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8a6d7-117">End of client support</span></span><br/> | <span data-ttu-id="8a6d7-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a6d7-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8a6d7-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8a6d7-119">End of server support</span></span><br/> | <span data-ttu-id="8a6d7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a6d7-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8a6d7-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8a6d7-121">Redistributable</span></span><br/>       | <span data-ttu-id="8a6d7-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a6d7-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8a6d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8a6d7-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8a6d7-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a6d7-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a6d7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a6d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6d7-126">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="8a6d7-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
