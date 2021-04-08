---
description: Ein "taubemmethodset"-Objekt ist eine Sammlung von "taubemmethod"-Objekten. Elemente werden mit der Item-Methode abgerufen. Weitere Informationen finden Sie unter Zugreifen auf eine Sammlung. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Taubemmethodset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865663"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="257af-106">Taubemmethodset-Objekt</span><span class="sxs-lookup"><span data-stu-id="257af-106">SWbemMethodSet object</span></span>

<span data-ttu-id="257af-107">Ein " **taubemmethodset** "-Objekt ist eine Sammlung von " [**taubemmethod**](swbemmethod.md) "-Objekten.</span><span class="sxs-lookup"><span data-stu-id="257af-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="257af-108">Elemente werden mit der [**Item**](swbemmethodset-item.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="257af-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="257af-109">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="257af-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="257af-110">Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="257af-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="257af-111">In dieser Version der API wird Schreibzugriff auf Methoden Informationen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="257af-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="257af-112">Wenn Sie Methoden definieren oder vorhandene Methoden Definitionen ändern möchten, können Sie die Methoden Änderungen in einer MOF-Datei definieren und die Änderungen mithilfe des MOF-Compilers übermitteln.</span><span class="sxs-lookup"><span data-stu-id="257af-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="257af-113">Alternativ können Sie die WMI-com-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="257af-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="257af-114">Member</span><span class="sxs-lookup"><span data-stu-id="257af-114">Members</span></span>

<span data-ttu-id="257af-115">Das Objekt " **Swap-methodset** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="257af-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="257af-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="257af-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="257af-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="257af-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="257af-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="257af-118">Methods</span></span>

<span data-ttu-id="257af-119">Das **taubemmethodset** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="257af-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="257af-120">Methode</span><span class="sxs-lookup"><span data-stu-id="257af-120">Method</span></span>                              | <span data-ttu-id="257af-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="257af-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="257af-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="257af-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="257af-123">Ruft [**ein-**](swbemmethod.md) Objekt aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="257af-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="257af-124">Dies ist die standardmäßige Automatisierungs Methode dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="257af-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="257af-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="257af-125">Properties</span></span>

<span data-ttu-id="257af-126">Das Objekt " **Swap-methodset** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="257af-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="257af-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="257af-127">Property</span></span>                                         | <span data-ttu-id="257af-128">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="257af-128">Access type</span></span>          | <span data-ttu-id="257af-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="257af-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="257af-130">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="257af-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="257af-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="257af-131">Read-only</span></span><br/> | <span data-ttu-id="257af-132">Die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="257af-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="257af-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="257af-133">Requirements</span></span>



| <span data-ttu-id="257af-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="257af-134">Requirement</span></span> | <span data-ttu-id="257af-135">Wert</span><span class="sxs-lookup"><span data-stu-id="257af-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="257af-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="257af-136">Minimum supported client</span></span><br/> | <span data-ttu-id="257af-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="257af-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="257af-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="257af-138">Minimum supported server</span></span><br/> | <span data-ttu-id="257af-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="257af-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="257af-140">Header</span><span class="sxs-lookup"><span data-stu-id="257af-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="257af-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="257af-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="257af-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="257af-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="257af-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="257af-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="257af-144">DLL</span><span class="sxs-lookup"><span data-stu-id="257af-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="257af-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="257af-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="257af-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="257af-146">CLSID</span></span><br/>                    | <span data-ttu-id="257af-147">CLSID- \_ Swap-Methode</span><span class="sxs-lookup"><span data-stu-id="257af-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="257af-148">IID</span><span class="sxs-lookup"><span data-stu-id="257af-148">IID</span></span><br/>                      | <span data-ttu-id="257af-149">IID \_ iswbemmethodset</span><span class="sxs-lookup"><span data-stu-id="257af-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="257af-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="257af-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257af-151">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="257af-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




