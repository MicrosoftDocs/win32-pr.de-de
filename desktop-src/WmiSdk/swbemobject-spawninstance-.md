---
description: Verwenden Sie zum Erstellen einer neuen Instanz einer-Klasse die SpawnInstance- \_ Methode des errbemubject-Objekts.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: SWbemObject.SpawnInstance_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218300"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="0b52d-103">Errbemubject. SpawnInstance- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="0b52d-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="0b52d-104">Verwenden Sie zum Erstellen einer neuen Instanz einer-Klasse die **SpawnInstance \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b52d-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="0b52d-105">Das aktuelle-Objekt muss eine Klassendefinition sein, die von WMI über eine Methode wie z. b. " [**Swap Services. Get**](swbemservices-get.md) " oder [**SWbemServices.Execquery**](swbemservices-execquery.md)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0b52d-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="0b52d-106">Verwenden Sie dann diese Klassendefinition, um neue Instanzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b52d-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="0b52d-107">Erstellen Sie jede neue Instanz lokal innerhalb des Prozesses, und rufen Sie dann " [**errbemubject. Put \_**](swbemobject-put-.md) " auf, um die Instanz in WMI tatsächlich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b52d-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="0b52d-108">Das Erzeugen einer Instanz aus einer-Instanz wird unterstützt, aber die zurückgegebene-Instanz ist leer.</span><span class="sxs-lookup"><span data-stu-id="0b52d-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="0b52d-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0b52d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b52d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b52d-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0b52d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b52d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b52d-112">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0b52d-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b52d-113">Reserviert und muss NULL sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b52d-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b52d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b52d-114">Return value</span></span>

<span data-ttu-id="0b52d-115">Wenn der Vorgang erfolgreich ist, gibt dieser-Befehl ein " [**errbemujebject**](swbemobject.md) "-Objekt mit einer neuen Instanz der-Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="0b52d-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b52d-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0b52d-116">Error codes</span></span>

<span data-ttu-id="0b52d-117">Nach dem Abschluss der **SpawnInstance \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b52d-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0b52d-118">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="0b52d-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="0b52d-119">Das aktuelle Objekt ist keine gültige Klassendefinition, und es kann keine neuen Instanzen erzeugen.</span><span class="sxs-lookup"><span data-stu-id="0b52d-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="0b52d-120">Entweder ist sie unvollständig, oder Sie wurde nicht bei WMI mithilfe von " [**errbemubject. Put \_**](swbemobject-put-.md)" registriert.</span><span class="sxs-lookup"><span data-stu-id="0b52d-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b52d-121">**wbemErrIllegalOperation** -2147749918 (0x8004101e)</span><span class="sxs-lookup"><span data-stu-id="0b52d-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="0b52d-122">Wird zurückgegeben, wenn diese Methode für eine-Instanz anstelle einer-Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b52d-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="0b52d-123">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0b52d-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0b52d-124">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b52d-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="0b52d-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0b52d-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0b52d-126">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0b52d-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b52d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b52d-127">Requirements</span></span>



| <span data-ttu-id="0b52d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b52d-128">Requirement</span></span> | <span data-ttu-id="0b52d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0b52d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b52d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b52d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0b52d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b52d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b52d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b52d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0b52d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b52d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b52d-134">Header</span><span class="sxs-lookup"><span data-stu-id="0b52d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b52d-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b52d-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b52d-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0b52d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b52d-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b52d-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b52d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0b52d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b52d-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b52d-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b52d-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="0b52d-140">CLSID</span></span><br/>                    | <span data-ttu-id="0b52d-141">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="0b52d-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0b52d-142">IID</span><span class="sxs-lookup"><span data-stu-id="0b52d-142">IID</span></span><br/>                      | <span data-ttu-id="0b52d-143">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="0b52d-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="0b52d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b52d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b52d-145">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="0b52d-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="0b52d-146">**Swap-Datei\_**</span><span class="sxs-lookup"><span data-stu-id="0b52d-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="0b52d-147">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="0b52d-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




