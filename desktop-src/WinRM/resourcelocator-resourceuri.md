---
title: ResourceLocator. resourceUri-Eigenschaft (WSManDisp. h)
description: Ruft den Ressourcen-URI in einem ResourceLocator-Objekt ab oder legt ihn fest.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceUri-Eigenschaft Windows-Remoteverwaltung
- ResourceUri-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, resourceUri-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477688"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="c435f-106">ResourceLocator. resourceUri (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c435f-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="c435f-107">Ruft den Ressourcen- [*URI*](windows-remote-management-glossary.md) in einem [**ResourceLocator**](resourcelocator.md) -Objekt ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="c435f-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="c435f-108">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c435f-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="c435f-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c435f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c435f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c435f-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="c435f-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c435f-111">Property value</span></span>

<span data-ttu-id="c435f-112">Eine Zeichenfolge, die die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c435f-112">A string that identifies the resource.</span></span> <span data-ttu-id="c435f-113">Wenn Sie den Ressourcen-URI für ein [**ResourceLocator**](resourcelocator.md) -Objekt festlegen, darf der URI nur den Pfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="c435f-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="c435f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c435f-114">Remarks</span></span>

<span data-ttu-id="c435f-115">Im folgenden finden Sie ein Beispiel für einen richtigen Pfad für [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="c435f-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="c435f-116">Der folgende Pfad funktioniert nicht, da er einen Schlüssel für eine bestimmte-Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="c435f-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="c435f-117">Verwenden Sie die [**ResourceLocator. addselector**](resourcelocator-addselector.md) -Methode, um eine bestimmte Instanz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c435f-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="c435f-118">**Iwsmanresourcelocator:: resourceUri** ist die entsprechende C++-Methode.</span><span class="sxs-lookup"><span data-stu-id="c435f-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c435f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c435f-119">Requirements</span></span>



| <span data-ttu-id="c435f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c435f-120">Requirement</span></span> | <span data-ttu-id="c435f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c435f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c435f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c435f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c435f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c435f-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c435f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c435f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c435f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c435f-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c435f-126">Header</span><span class="sxs-lookup"><span data-stu-id="c435f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c435f-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c435f-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c435f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="c435f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c435f-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c435f-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c435f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c435f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c435f-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c435f-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c435f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c435f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c435f-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c435f-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c435f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c435f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c435f-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="c435f-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





