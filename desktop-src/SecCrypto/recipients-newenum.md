---
description: Die \_ Eigenschaft "netwenum" der Empfänger Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357605"
---
# <a name="recipients_newenum-property"></a><span data-ttu-id="56dc9-104">Empfänger. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="56dc9-104">Recipients.\_NewEnum property</span></span>

<span data-ttu-id="56dc9-105">\[Die Eigenschaft " **\_ netwenum** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="56dc9-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56dc9-106">Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="56dc9-106">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="56dc9-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="56dc9-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="56dc9-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="56dc9-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="56dc9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="56dc9-109">Syntax</span></span>


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="56dc9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56dc9-110">Property value</span></span>

<span data-ttu-id="56dc9-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="56dc9-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="56dc9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56dc9-112">Remarks</span></span>

<span data-ttu-id="56dc9-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="56dc9-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="56dc9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56dc9-114">Requirements</span></span>



| <span data-ttu-id="56dc9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56dc9-115">Requirement</span></span> | <span data-ttu-id="56dc9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="56dc9-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56dc9-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="56dc9-117">Redistributable</span></span><br/> | <span data-ttu-id="56dc9-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="56dc9-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56dc9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="56dc9-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="56dc9-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56dc9-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dc9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56dc9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dc9-122">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="56dc9-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
