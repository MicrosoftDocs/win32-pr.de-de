---
description: Führt eine Abfrage zum Empfangen von Ereignissen aus. Der-Rückruf wird sofort zurückgegeben.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Execnotificationquery-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363518"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="63ba6-104">SWbemServices.Execnotificationquery-Methode</span><span class="sxs-lookup"><span data-stu-id="63ba6-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="63ba6-105">Die **ExecNotificationQuery** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Abfrage zum Empfangen von Ereignissen aus.</span><span class="sxs-lookup"><span data-stu-id="63ba6-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="63ba6-106">Der-Rückruf wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63ba6-106">The call returns immediately.</span></span> <span data-ttu-id="63ba6-107">Der Benutzer kann den zurückgegebenen Enumerator nach Ereignissen abrufen, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="63ba6-108">Die-Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="63ba6-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="63ba6-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="63ba6-110">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="63ba6-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63ba6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="63ba6-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="63ba6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63ba6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ba6-113">*"-Abfrage"*</span><span class="sxs-lookup"><span data-stu-id="63ba6-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="63ba6-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63ba6-114">Required.</span></span> <span data-ttu-id="63ba6-115">Eine Zeichenfolge, die den Text der ereignisbezogenen Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="63ba6-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="63ba6-116">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="63ba6-116">This parameter cannot be blank.</span></span> <span data-ttu-id="63ba6-117">Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="63ba6-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-118">"in der *Sprache* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="63ba6-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-119">Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält.</span><span class="sxs-lookup"><span data-stu-id="63ba6-119">String that contains the query language to be used.</span></span> <span data-ttu-id="63ba6-120">Wenn angegeben, muss dieser Wert "WQL" lauten.</span><span class="sxs-lookup"><span data-stu-id="63ba6-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-121">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="63ba6-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-122">Dies ist eine ganze Zahl, die das Verhalten der Abfrage bestimmt.</span><span class="sxs-lookup"><span data-stu-id="63ba6-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="63ba6-123">Der Standardwert ist **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="63ba6-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="63ba6-124">Wenn Sie diesen Parameter angeben, muss dieser Parameter sowohl auf **wbemFlagReturnImmediately** als auch auf **wbemFlagForwardOnly** festgelegt werden, andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="63ba6-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="63ba6-125">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="63ba6-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="63ba6-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="63ba6-127">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="63ba6-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="63ba6-128">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="63ba6-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="63ba6-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="63ba6-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="63ba6-130">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="63ba6-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="63ba6-131">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="63ba6-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-132">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="63ba6-132">Typically, this is undefined.</span></span> <span data-ttu-id="63ba6-133">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="63ba6-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="63ba6-134">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="63ba6-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ba6-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63ba6-135">Return value</span></span>

<span data-ttu-id="63ba6-136">Wenn kein Fehler auftritt, gibt diese Methode ein " [**errbemeventsource**](swbemeventsource.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="63ba6-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="63ba6-137">Sie können die Methode " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md) " aufrufen, um Ereignisse abzurufen, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63ba6-138">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="63ba6-138">Error codes</span></span>

<span data-ttu-id="63ba6-139">Nach dem Abschluss der **ExecNotificationQuery** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="63ba6-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="63ba6-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="63ba6-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-141">Der aktuelle Benutzer ist nicht autorisiert, das Resultset anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="63ba6-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-143">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="63ba6-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-144">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="63ba6-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-145">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="63ba6-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-146">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="63ba6-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-147">Die Abfrage Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="63ba6-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="63ba6-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-149">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63ba6-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="63ba6-150">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="63ba6-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="63ba6-151">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="63ba6-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63ba6-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63ba6-152">Remarks</span></span>

<span data-ttu-id="63ba6-153">Anders als bei der [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md) -Methode gibt **ExecNotificationQuery** Ereignistyp Objekte zurück, die von zukünftigen Ereignissen generiert werden, und nicht von vorhandenen Objekten.</span><span class="sxs-lookup"><span data-stu-id="63ba6-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="63ba6-154">Die Ereignis Objekte, die von **ExecNotificationQuery** angefordert werden, können System intern (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder Extrinsisch (z. b. Registrierungs Anbieter Ereignisse wie z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) oder SNMP-Ereignisse) sein.</span><span class="sxs-lookup"><span data-stu-id="63ba6-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="63ba6-155">Weitere Informationen finden Sie unter [bestimmen des Ereignis Typs zum empfangen](determining-the-type-of-event-to-receive.md) und [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="63ba6-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="63ba6-156">Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="63ba6-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="63ba6-157">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="63ba6-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="63ba6-158">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="63ba6-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="63ba6-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63ba6-159">Examples</span></span>

<span data-ttu-id="63ba6-160">Im folgenden VBScript-Codebeispiel werden Änderungen an Volumes auf einem lokalen Computer überwacht.</span><span class="sxs-lookup"><span data-stu-id="63ba6-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="63ba6-161">Beachten Sie, dass [**Win32 \_ volumechangeevent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) ein extrinsisches Ereignis ist, das von einem Anbieter definiert wird, der kein System internes, von WMI definiertes Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="63ba6-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="63ba6-162">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="63ba6-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="63ba6-163">Im folgenden VBScript-Codebeispiel wird der Prozess Löschvorgang überwacht.</span><span class="sxs-lookup"><span data-stu-id="63ba6-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="63ba6-164">Wenn Sie einen Prozess im Task-Manager löschen oder eine Anwendung schließen, zeigt das Skript eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="63ba6-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="63ba6-165">Beachten Sie, dass dieses Skript ein System internes Ereignis abfragt, das von WMI- [**\_ \_ instancedeletionevent**](--instancedeletionevent.md)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="63ba6-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="63ba6-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63ba6-166">Requirements</span></span>



| <span data-ttu-id="63ba6-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63ba6-167">Requirement</span></span> | <span data-ttu-id="63ba6-168">Wert</span><span class="sxs-lookup"><span data-stu-id="63ba6-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba6-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63ba6-169">Minimum supported client</span></span><br/> | <span data-ttu-id="63ba6-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63ba6-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63ba6-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63ba6-171">Minimum supported server</span></span><br/> | <span data-ttu-id="63ba6-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63ba6-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63ba6-173">Header</span><span class="sxs-lookup"><span data-stu-id="63ba6-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="63ba6-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ba6-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="63ba6-175">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="63ba6-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="63ba6-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63ba6-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63ba6-177">DLL</span><span class="sxs-lookup"><span data-stu-id="63ba6-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63ba6-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ba6-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63ba6-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="63ba6-179">CLSID</span></span><br/>                    | <span data-ttu-id="63ba6-180">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="63ba6-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="63ba6-181">IID</span><span class="sxs-lookup"><span data-stu-id="63ba6-181">IID</span></span><br/>                      | <span data-ttu-id="63ba6-182">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="63ba6-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="63ba6-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63ba6-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ba6-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="63ba6-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="63ba6-185">**"Errbemeventsource. NextEvent"**</span><span class="sxs-lookup"><span data-stu-id="63ba6-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="63ba6-186">**CquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="63ba6-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="63ba6-187">Empfangen eines WMI-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="63ba6-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="63ba6-188">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="63ba6-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="63ba6-189">WQL (SQL für WMI)</span><span class="sxs-lookup"><span data-stu-id="63ba6-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="63ba6-190">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="63ba6-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

