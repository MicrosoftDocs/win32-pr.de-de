---
title: ResourceLocator. mustverständlicherweise Options-Eigenschaft (WSManDisp. h)
description: Ruft den mustverständlicherweise Options-Wert für das ResourceLocator-Objekt ab oder legt ihn fest.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Mustverständlicherweise Options-Eigenschaft Windows-Remoteverwaltung
- Mustverständlicherweise Options-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, mustverständlicherweise Options-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957051"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="35a40-106">ResourceLocator. mustverständlicherweise Options-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35a40-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="35a40-107">Ruft den **mustverständlicherweise Options** -Wert für das [**ResourceLocator**](resourcelocator.md) -Objekt ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="35a40-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="35a40-108">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="35a40-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="35a40-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="35a40-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a40-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="35a40-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="35a40-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35a40-111">Property value</span></span>

<span data-ttu-id="35a40-112">Gibt an, dass der Dienst, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert, beim Wert " **true**" einen Fehler zurückgeben muss, wenn er die Option nicht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="35a40-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a40-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35a40-113">Remarks</span></span>

<span data-ttu-id="35a40-114">**Iwsmanresourcelocator:: mustverständlicherweise Options** ist die entsprechende C++-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="35a40-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a40-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a40-115">Requirements</span></span>



| <span data-ttu-id="35a40-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a40-116">Requirement</span></span> | <span data-ttu-id="35a40-117">Wert</span><span class="sxs-lookup"><span data-stu-id="35a40-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a40-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35a40-118">Minimum supported client</span></span><br/> | <span data-ttu-id="35a40-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35a40-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="35a40-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35a40-120">Minimum supported server</span></span><br/> | <span data-ttu-id="35a40-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a40-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="35a40-122">Header</span><span class="sxs-lookup"><span data-stu-id="35a40-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a40-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a40-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35a40-124">IDL</span><span class="sxs-lookup"><span data-stu-id="35a40-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35a40-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35a40-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="35a40-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35a40-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="35a40-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35a40-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35a40-128">DLL</span><span class="sxs-lookup"><span data-stu-id="35a40-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a40-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a40-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35a40-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a40-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="35a40-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





