---
description: Die-Schnittstelle von "ikspropertyset" wurde ursprünglich als effiziente Methode zum Festlegen und Abrufen von Geräteeigenschaften für WDM-Treiber entwickelt. dabei wurde ksproxy verwendet, um die com-Methodenaufrufe im Benutzermodus in die Kernel Modus-Eigenschaften Sätze zu übersetzen, die von WDM-Streaming-Klassen Treibern Diese Schnittstelle wird jetzt auch verwendet, um Informationen genau zwischen Softwarekomponenten zu übergeben. In einigen Fällen müssen Softwarekomponenten diese Schnittstelle oder andernfalls die "ikscontrol"-Schnittstelle implementieren (im DirectShow-DDK dokumentiert). Wenn Sie z. b. einen Software-MPEG-2-Decoder für die Verwendung mit dem DVD-Navigator schreiben, müssen Sie eine dieser Schnittstellen implementieren und außerdem die DVD-bezogenen Eigenschaften Sätze unterstützen, die der Navigator an den Decoder sendet. Pins können eine dieser Schnittstellen unterstützen, damit andere Pins oder Filter Ihre Eigenschaften festlegen oder abrufen können. Beachten Sie, dass in der DSound. h-Header Datei eine andere Schnittstelle mit diesem Namen vorhanden ist. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte "ikscontrol"-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: "' Ikspropertyset '-Schnittstelle (ksproxy. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480771"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="08536-109">"Ikspropertyset"-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="08536-109">IKsPropertySet interface</span></span>

<span data-ttu-id="08536-110">Die `IKsPropertySet` -Schnittstelle wurde ursprünglich als effiziente Methode zum Festlegen und Abrufen von Geräteeigenschaften für WDM-Treiber entwickelt. dabei wurde ksproxy verwendet, um die com-Methodenaufrufe im Benutzermodus in die Kernel Modus-Eigenschaften Sätze zu übersetzen, die von WDM-Streaming-Klassen Treibern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08536-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="08536-111">Diese Schnittstelle wird jetzt auch verwendet, um Informationen genau zwischen Softwarekomponenten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="08536-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="08536-112">In einigen Fällen müssen Softwarekomponenten diese Schnittstelle oder andernfalls die " **ikscontrol** "-Schnittstelle implementieren (im DirectShow-DDK dokumentiert).</span><span class="sxs-lookup"><span data-stu-id="08536-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="08536-113">Wenn Sie z. b. einen Software-MPEG-2-Decoder für die Verwendung mit dem [DVD-Navigator](dvd-navigator-filter.md)schreiben, müssen Sie eine dieser Schnittstellen implementieren und außerdem die DVD-bezogenen Eigenschaften Sätze unterstützen, die der Navigator an den Decoder sendet.</span><span class="sxs-lookup"><span data-stu-id="08536-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="08536-114">Pins können eine dieser Schnittstellen unterstützen, damit andere Pins oder Filter Ihre Eigenschaften festlegen oder abrufen können.</span><span class="sxs-lookup"><span data-stu-id="08536-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="08536-115">Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="08536-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="08536-116">Die beiden Schnittstellen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="08536-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="08536-117">Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.</span><span class="sxs-lookup"><span data-stu-id="08536-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="08536-118">Member</span><span class="sxs-lookup"><span data-stu-id="08536-118">Members</span></span>

<span data-ttu-id="08536-119">Die " **ikspropertyset** "-Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="08536-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="08536-120">" **Ikspropertyset** " verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08536-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="08536-121">Methoden</span><span class="sxs-lookup"><span data-stu-id="08536-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="08536-122">Methoden</span><span class="sxs-lookup"><span data-stu-id="08536-122">Methods</span></span>

<span data-ttu-id="08536-123">Die " **ikspropertyset** "-Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="08536-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="08536-124">Methode</span><span class="sxs-lookup"><span data-stu-id="08536-124">Method</span></span>                                                  | <span data-ttu-id="08536-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08536-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="08536-126">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="08536-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="08536-127">Ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="08536-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="08536-128">**Querysupported**</span><span class="sxs-lookup"><span data-stu-id="08536-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="08536-129">Bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08536-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="08536-130">**Set**</span><span class="sxs-lookup"><span data-stu-id="08536-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="08536-131">Legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="08536-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="08536-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08536-132">Remarks</span></span>

<span data-ttu-id="08536-133">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="08536-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="08536-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08536-134">Requirements</span></span>



| <span data-ttu-id="08536-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08536-135">Requirement</span></span> | <span data-ttu-id="08536-136">Wert</span><span class="sxs-lookup"><span data-stu-id="08536-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08536-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08536-137">Minimum supported client</span></span><br/> | <span data-ttu-id="08536-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08536-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08536-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08536-139">Minimum supported server</span></span><br/> | <span data-ttu-id="08536-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08536-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08536-141">Header</span><span class="sxs-lookup"><span data-stu-id="08536-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="08536-142"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="08536-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="08536-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08536-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="08536-144"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="08536-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08536-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08536-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08536-146">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="08536-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
