---
description: Die \_ Eigenschaft "netwenum" von "ExtendedProperties" Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: ExtendedProperties._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372421"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="df346-104">ExtendedProperties. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="df346-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="df346-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df346-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="df346-106">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktion [**certgetcertifierecontextproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df346-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="df346-107">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="df346-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="df346-108">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="df346-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="df346-109">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df346-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="df346-110">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="df346-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="df346-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="df346-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="df346-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="df346-112">Property value</span></span>

<span data-ttu-id="df346-113">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df346-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="df346-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df346-114">Remarks</span></span>

<span data-ttu-id="df346-115">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="df346-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="df346-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df346-116">Requirements</span></span>



| <span data-ttu-id="df346-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df346-117">Requirement</span></span> | <span data-ttu-id="df346-118">Wert</span><span class="sxs-lookup"><span data-stu-id="df346-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df346-119">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="df346-119">End of client support</span></span><br/> | <span data-ttu-id="df346-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df346-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df346-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="df346-121">End of server support</span></span><br/> | <span data-ttu-id="df346-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df346-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df346-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="df346-123">Redistributable</span></span><br/>       | <span data-ttu-id="df346-124">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="df346-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="df346-125">DLL</span><span class="sxs-lookup"><span data-stu-id="df346-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="df346-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df346-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
