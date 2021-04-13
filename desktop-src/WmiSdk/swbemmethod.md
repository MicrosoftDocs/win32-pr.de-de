---
description: Sie können die Eigenschaften des Objekts "Swap Method" verwenden, um eine einzelne Methoden Definition eines WMI-Objekts zu überprüfen. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Taubemmethod-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528487"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="43447-104">Taubemmethod-Objekt</span><span class="sxs-lookup"><span data-stu-id="43447-104">SWbemMethod object</span></span>

<span data-ttu-id="43447-105">Sie können die Eigenschaften des Objekts " **Swap Method** " verwenden, um eine einzelne Methoden Definition eines WMI-Objekts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="43447-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="43447-106">Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="43447-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="43447-107">Dieses Objekt kann verwendet werden, um die Definitionen von-Methoden zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="43447-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="43447-108">Um die Methoden aufzurufen, sollten Sie entweder den direkten Zugriff (siehe Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md)) für ein " [**errbemubject**](swbemobject.md) " (das empfohlene Mechanismus) oder den [**SWbemServices.Execmethod**](swbemservices-execmethod.md) -Aufruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="43447-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="43447-109">In dieser Version der API wird Schreibzugriff auf Methoden Informationen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43447-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="43447-110">Wenn Sie Methoden definieren oder vorhandene Methoden Definitionen ändern möchten, können Sie die Methoden Änderungen in einer MOF-Datei definieren und die Änderungen mithilfe des [MOF-Compilers](compiling-mof-files.md)übermitteln.</span><span class="sxs-lookup"><span data-stu-id="43447-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="43447-111">Verwenden Sie alternativ die [com-API für WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="43447-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="43447-112">Member</span><span class="sxs-lookup"><span data-stu-id="43447-112">Members</span></span>

<span data-ttu-id="43447-113">Das Objekt " **Swap-Methode** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="43447-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="43447-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43447-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43447-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43447-115">Properties</span></span>

<span data-ttu-id="43447-116">Das Objekt " **Swap-Methode** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43447-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="43447-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="43447-117">Property</span></span>                                                      | <span data-ttu-id="43447-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="43447-118">Access type</span></span>          | <span data-ttu-id="43447-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43447-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43447-120">**InParameters**</span><span class="sxs-lookup"><span data-stu-id="43447-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="43447-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43447-121">Read-only</span></span><br/> | <span data-ttu-id="43447-122">Ein [**-**](swbemobject.md) Objekt, dessen Eigenschaften die Eingabeparameter für diese Methode definieren.</span><span class="sxs-lookup"><span data-stu-id="43447-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="43447-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="43447-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="43447-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43447-124">Read-only</span></span><br/> | <span data-ttu-id="43447-125">Der Name der Methode.</span><span class="sxs-lookup"><span data-stu-id="43447-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="43447-126">**Entstehungs**</span><span class="sxs-lookup"><span data-stu-id="43447-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="43447-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43447-127">Read-only</span></span><br/> | <span data-ttu-id="43447-128">Die Ursprungs Klasse der Methode.</span><span class="sxs-lookup"><span data-stu-id="43447-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="43447-129">**OutParameters**</span><span class="sxs-lookup"><span data-stu-id="43447-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="43447-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43447-130">Read-only</span></span><br/> | <span data-ttu-id="43447-131">Ein [**-**](swbemobject.md) Objekt, dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren.</span><span class="sxs-lookup"><span data-stu-id="43447-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="43447-132">**Qualifikation\_**</span><span class="sxs-lookup"><span data-stu-id="43447-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="43447-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="43447-133">Read-only</span></span><br/> | <span data-ttu-id="43447-134">Ein [**-**](swbemqualifierset.md) Objekt, das die Qualifizierer für diese Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="43447-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="43447-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43447-135">Requirements</span></span>



| <span data-ttu-id="43447-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43447-136">Requirement</span></span> | <span data-ttu-id="43447-137">Wert</span><span class="sxs-lookup"><span data-stu-id="43447-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43447-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43447-138">Minimum supported client</span></span><br/> | <span data-ttu-id="43447-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43447-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43447-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43447-140">Minimum supported server</span></span><br/> | <span data-ttu-id="43447-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43447-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43447-142">Header</span><span class="sxs-lookup"><span data-stu-id="43447-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="43447-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43447-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43447-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="43447-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="43447-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43447-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43447-146">DLL</span><span class="sxs-lookup"><span data-stu-id="43447-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43447-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43447-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="43447-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="43447-148">CLSID</span></span><br/>                    | <span data-ttu-id="43447-149">CLSID- \_ Swap-Methode</span><span class="sxs-lookup"><span data-stu-id="43447-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="43447-150">IID</span><span class="sxs-lookup"><span data-stu-id="43447-150">IID</span></span><br/>                      | <span data-ttu-id="43447-151">IID \_ iswbemmethod</span><span class="sxs-lookup"><span data-stu-id="43447-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="43447-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43447-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43447-153">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="43447-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




