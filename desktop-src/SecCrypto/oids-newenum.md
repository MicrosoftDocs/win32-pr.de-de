---
description: Die \_ Eigenschaft "netwenum" von OIDs Ruft eine IEnumVARIANT-Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: OIDs._NewEnum-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366895"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="e6e89-104">OIDs. \_ Eigenschaft "netwenum"</span><span class="sxs-lookup"><span data-stu-id="e6e89-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="e6e89-105">\[Die Eigenschaft " **\_ netwenum** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e6e89-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e6e89-106">Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e6e89-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e6e89-107">Die Eigenschaft " **\_ netwenum** " Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6e89-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e6e89-108">Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e6e89-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e89-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6e89-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="e6e89-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e6e89-110">Property value</span></span>

<span data-ttu-id="e6e89-111">Eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt, das zum Auflisten der Auflistung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6e89-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e89-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6e89-112">Remarks</span></span>

<span data-ttu-id="e6e89-113">Diese Eigenschaft wird automatisch intern verwendet, wenn Sie das- `For Each In` Konstrukt in Visual Basic Scripting Edition (VBScript) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6e89-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e89-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e89-114">Requirements</span></span>



| <span data-ttu-id="e6e89-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e89-115">Requirement</span></span> | <span data-ttu-id="e6e89-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e89-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e89-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e6e89-117">Redistributable</span></span><br/> | <span data-ttu-id="e6e89-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6e89-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e6e89-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e6e89-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="e6e89-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6e89-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e89-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e89-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e89-122">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="e6e89-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
