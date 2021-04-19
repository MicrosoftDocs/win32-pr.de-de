---
description: Die \_ Eigenschaft "netwenum" der Signatur Geber Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366839"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="f4209-104">Signatur Geber. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="f4209-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="f4209-105">\[Die Eigenschaft " **\_ netwenum** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f4209-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4209-106">Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten.</span><span class="sxs-lookup"><span data-stu-id="f4209-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="f4209-107">Weitere Informationen finden Sie unter der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f4209-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f4209-108">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4209-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f4209-109">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="f4209-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4209-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4209-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="f4209-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f4209-111">Property value</span></span>

<span data-ttu-id="f4209-112">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4209-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4209-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4209-113">Remarks</span></span>

<span data-ttu-id="f4209-114">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4209-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4209-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4209-115">Requirements</span></span>



| <span data-ttu-id="f4209-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4209-116">Requirement</span></span> | <span data-ttu-id="f4209-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4209-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4209-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f4209-118">Redistributable</span></span><br/> | <span data-ttu-id="f4209-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4209-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f4209-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f4209-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="f4209-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4209-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4209-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4209-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4209-123">**Signatur Geber**</span><span class="sxs-lookup"><span data-stu-id="f4209-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
