---
description: Ruft ein-Objekt ab, das entweder eine Klassendefinition oder eine-Instanz ist, basierend auf dem Objekt Pfad.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: Swap Services. Get-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349271"
---
# <a name="swbemservicesget-method"></a><span data-ttu-id="d3f75-103">Methode "Swap Services. Get"</span><span class="sxs-lookup"><span data-stu-id="d3f75-103">SWbemServices.Get method</span></span>

<span data-ttu-id="d3f75-104">Mit der **Get** -Methode des-Objekts " [**Swap Services**](swbemservices.md) " wird ein-Objekt abgerufen, das entweder eine Klassendefinition oder eine-Instanz ist, die auf dem Objekt Pfad basiert.</span><span class="sxs-lookup"><span data-stu-id="d3f75-104">The **Get** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is either a class definition or an instance, based on the object path.</span></span> <span data-ttu-id="d3f75-105">Diese Methode ruft nur Objekte aus dem Namespace ab, der dem aktuellen ' **Swap Services** '-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3f75-105">This method retrieves only objects from the namespace that is associated with the current **SWbemServices** object.</span></span>

<span data-ttu-id="d3f75-106">Die-Methode wird im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d3f75-106">The method is called in the synchronous mode.</span></span> <span data-ttu-id="d3f75-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d3f75-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d3f75-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d3f75-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f75-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f75-109">Syntax</span></span>


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d3f75-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f75-111">*strobjectpath* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d3f75-111">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-112">Eine Zeichenfolge, die den Objekt Pfad des abzurufenden-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="d3f75-112">String that contains the object path of the object to retrieve.</span></span> <span data-ttu-id="d3f75-113">Wenn dieser Wert leer ist, kann das leere Objekt, das zurückgegeben wird, eine neue Klasse werden.</span><span class="sxs-lookup"><span data-stu-id="d3f75-113">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="d3f75-114">Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="d3f75-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-115">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d3f75-115">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-116">Eine ganze Zahl, die das Verhalten der Abfrage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-116">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="d3f75-117">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d3f75-117">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d3f75-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d3f75-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d3f75-119">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-119">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="d3f75-120">Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d3f75-120">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d3f75-121">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d3f75-121">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-122">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d3f75-122">Typically, this is undefined.</span></span> <span data-ttu-id="d3f75-123">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d3f75-123">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d3f75-124">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="d3f75-124">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f75-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3f75-125">Return value</span></span>

<span data-ttu-id="d3f75-126">Wenn der [**Vorgang**](swbemobject.md) erfolgreich ist, gibt diese Methode ein-Objekt zurück, das das angeforderte Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-126">If successful, this method returns an [**SWbemObject**](swbemobject.md) object that represents the requested object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3f75-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d3f75-127">Error codes</span></span>

<span data-ttu-id="d3f75-128">Nach Abschluss der **Get** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3f75-128">Upon the completion of the **Get** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d3f75-129">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d3f75-129">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-130">Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-130">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-131">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d3f75-131">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-132">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d3f75-132">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d3f75-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-134">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d3f75-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-135">**wbemErrInvalidObjectPath** -2147749946 (0x8004103a)</span><span class="sxs-lookup"><span data-stu-id="d3f75-135">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-136">Der angegebene Pfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="d3f75-136">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-137">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="d3f75-137">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-138">Das angeforderte Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d3f75-138">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="d3f75-139">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d3f75-139">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d3f75-140">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d3f75-140">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3f75-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3f75-141">Remarks</span></span>

<span data-ttu-id="d3f75-142">Im Gegensatz zu den Methoden [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) und [**InstancesOf**](swbemservices-instancesof.md) gibt die Get-Methode immer ein- [**Objekt**](swbemobject.md) zurück, das eine bestimmte Instanz einer von WMI verwalteten Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-142">Unlike the [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) and [**InstancesOf**](swbemservices-instancesof.md) methods, the Get method always returns an [**SWbemObject**](swbemobject.md) representing a specific instance of a WMI-managed resource.</span></span> <span data-ttu-id="d3f75-143">Zum Abrufen einer bestimmten Instanz einer durch WMI verwalteten Ressource mithilfe der Get-Methode müssen Sie die abzurufende Instanz abrufen, indem Sie die-Methode den Objekt Pfad übergeben, wie im folgenden Skript gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3f75-143">To obtain a specific instance of a WMI-managed resource using the Get method, you must tell Get the instance to retrieve by passing the method the object path, as shown in the following script.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



<span data-ttu-id="d3f75-144">Mit dieser Methode können Sie [*Singleton*](gloss-s.md) -Objekte, z. b. [**\_ \_ cimumidentifizierung**](--cimomidentification.md), mit Versionsinformationen zur WMI-Installation, die ausgeführt wird, abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3f75-144">You can use this method to obtain [*singleton*](gloss-s.md) objects, such as [**\_\_CIMOMIdentification**](--cimomidentification.md), which contains version information about the WMI installation that is running.</span></span>

<span data-ttu-id="d3f75-145">Sie können das Repository mit einem Anzeige Tool wie [CIM Studio](further-information.md) untersuchen, um zu überprüfen, ob die neue Klasse und Instanz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f75-145">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="d3f75-146">Ein Beispiel für das Entfernen einer Klasse und einer Instanz aus dem Repository finden Sie unter " [**errbemservices. Delete**](swbemservices-delete.md) " oder " [**errbemubject. Delete \_**](swbemobject-delete-.md)".</span><span class="sxs-lookup"><span data-stu-id="d3f75-146">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f75-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3f75-147">Requirements</span></span>



| <span data-ttu-id="d3f75-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3f75-148">Requirement</span></span> | <span data-ttu-id="d3f75-149">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f75-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f75-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3f75-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f75-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3f75-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3f75-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3f75-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f75-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3f75-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3f75-154">Header</span><span class="sxs-lookup"><span data-stu-id="d3f75-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f75-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f75-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3f75-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d3f75-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3f75-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d3f75-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d3f75-158">DLL</span><span class="sxs-lookup"><span data-stu-id="d3f75-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3f75-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3f75-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3f75-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="d3f75-160">CLSID</span></span><br/>                    | <span data-ttu-id="d3f75-161">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="d3f75-161">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d3f75-162">IID</span><span class="sxs-lookup"><span data-stu-id="d3f75-162">IID</span></span><br/>                      | <span data-ttu-id="d3f75-163">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="d3f75-163">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d3f75-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3f75-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f75-165">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d3f75-165">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d3f75-166">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="d3f75-166">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




