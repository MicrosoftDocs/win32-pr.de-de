---
title: ResourceLocator. fragmentpath-Eigenschaft (WSManDisp. h)
description: Ruft den Pfad für ein Ressourcen Fragment oder eine Ressourcen Eigenschaft ab oder legt diesen fest, wenn ResourceLocator in Sitzungs Objekt Vorgängen verwendet wird, z. b. Session. Get, Session. Put oder Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Fragmentpath-Eigenschaft Windows-Remoteverwaltung
- Fragmentpath-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, fragmentpath-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040647"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="66572-106">ResourceLocator. fragmentpath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66572-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="66572-107">Ruft den Pfad für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) oder eine Ressourcen Eigenschaft ab oder legt diesen fest, wenn [**ResourceLocator**](resourcelocator.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwendet wird, z. b [**. Session. Get**](session-get.md), [**Session. Put**](session-put.md)oder [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="66572-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="66572-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="66572-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66572-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="66572-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="66572-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="66572-110">Property value</span></span>

<span data-ttu-id="66572-111">Eine Zeichenfolge, die das Fragment oder die Eigenschaft der Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66572-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="66572-112">Wenn die Ressource z. b. ein Laufwerk ist und die angeforderte Eigenschaft Hersteller ist, kann die Zeichenfolge enthalten `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="66572-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="66572-113">Beim Fragmenttext wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="66572-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="66572-114">In diesem Fall können Sie nicht verwenden `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="66572-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="66572-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66572-115">Remarks</span></span>

<span data-ttu-id="66572-116">**Iwsmanresourcelocator:: fragmentpath** ist die entsprechende C++-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="66572-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="66572-117">Sie können ein Element einer Array Eigenschaft angeben, indem Sie den Array Index bereitstellen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="66572-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="66572-118">Beachten Sie, dass die Array Indizierung mit 1 statt 0 beginnt.</span><span class="sxs-lookup"><span data-stu-id="66572-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="66572-119">Um das gesamte Array zu erhalten, geben Sie den Namen der Array Eigenschaft an, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="66572-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="66572-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66572-120">Requirements</span></span>



| <span data-ttu-id="66572-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66572-121">Requirement</span></span> | <span data-ttu-id="66572-122">Wert</span><span class="sxs-lookup"><span data-stu-id="66572-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66572-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66572-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66572-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66572-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="66572-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66572-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66572-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66572-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="66572-127">Header</span><span class="sxs-lookup"><span data-stu-id="66572-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66572-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="66572-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="66572-129">IDL</span><span class="sxs-lookup"><span data-stu-id="66572-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66572-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66572-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="66572-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66572-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="66572-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="66572-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="66572-133">DLL</span><span class="sxs-lookup"><span data-stu-id="66572-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66572-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66572-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66572-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66572-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66572-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="66572-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





