---
description: Erweitert die Funktionalität von Swap Services.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Taubemservicesex-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130972"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="5db79-103">Taubemservicesex-Objekt</span><span class="sxs-lookup"><span data-stu-id="5db79-103">SWbemServicesEx object</span></span>

<span data-ttu-id="5db79-104">Das Objekt " **taubemservicesex** " erweitert die Funktionalität von " [**Swap Services**](swbemservices.md)".</span><span class="sxs-lookup"><span data-stu-id="5db79-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="5db79-105">Die [**Put**](swbemservicesex-put.md) -Methode und die [**putasync**](swbemservicesex-putasync.md) -Methode ermöglichen es, eine Klasse oder eine Instanz in mehreren Namespaces oder in einem anderen Namespace als dem zu speichern, in dem eine Instanz erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5db79-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="5db79-106">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5db79-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="5db79-107">Member</span><span class="sxs-lookup"><span data-stu-id="5db79-107">Members</span></span>

<span data-ttu-id="5db79-108">Das Objekt " **taubemservicesex** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5db79-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="5db79-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="5db79-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5db79-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="5db79-110">Methods</span></span>

<span data-ttu-id="5db79-111">Das Objekt " **taubemservicesex** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5db79-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="5db79-112">Methode</span><span class="sxs-lookup"><span data-stu-id="5db79-112">Method</span></span>                                       | <span data-ttu-id="5db79-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5db79-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5db79-114">**Stellte**</span><span class="sxs-lookup"><span data-stu-id="5db79-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="5db79-115">Speichert das Objekt in dem Namespace, der an das Objekt " **errbemservicesex** " gebunden ist, und gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="5db79-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="5db79-116">**Putasync**</span><span class="sxs-lookup"><span data-stu-id="5db79-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="5db79-117">Speichert ein-Objekt asynchron in einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="5db79-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5db79-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5db79-118">Remarks</span></span>

<span data-ttu-id="5db79-119">Die Methoden in dieser Klasse können entweder im semisynchronen oder im asynchronen Modus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5db79-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="5db79-120">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5db79-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5db79-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5db79-121">Requirements</span></span>



| <span data-ttu-id="5db79-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5db79-122">Requirement</span></span> | <span data-ttu-id="5db79-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5db79-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db79-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5db79-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5db79-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5db79-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5db79-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5db79-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5db79-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5db79-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5db79-128">Header</span><span class="sxs-lookup"><span data-stu-id="5db79-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db79-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db79-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5db79-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5db79-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="5db79-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5db79-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5db79-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5db79-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5db79-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5db79-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5db79-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="5db79-134">CLSID</span></span><br/>                    | <span data-ttu-id="5db79-135">CLSID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="5db79-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="5db79-136">IID</span><span class="sxs-lookup"><span data-stu-id="5db79-136">IID</span></span><br/>                      | <span data-ttu-id="5db79-137">IID \_ iswbemservicesex</span><span class="sxs-lookup"><span data-stu-id="5db79-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5db79-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5db79-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db79-139">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="5db79-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="5db79-140">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="5db79-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

