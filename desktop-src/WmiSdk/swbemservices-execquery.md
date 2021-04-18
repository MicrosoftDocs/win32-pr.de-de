---
description: Führt eine Abfrage zum Abrufen von Objekten aus.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Execquery-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359099"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="1783d-103">SWbemServices.Execquery-Methode</span><span class="sxs-lookup"><span data-stu-id="1783d-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="1783d-104">Die **ExecQuery** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Abfrage zum Abrufen von-Objekten aus.</span><span class="sxs-lookup"><span data-stu-id="1783d-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="1783d-105">Diese Objekte sind über die zurückgegebene [**errbewbjectset**](swbemobjectset.md) -Auflistung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1783d-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="1783d-106">Diese Methode wird im semisynchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1783d-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="1783d-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1783d-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1783d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1783d-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1783d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1783d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1783d-111">*"-Abfrage"*</span><span class="sxs-lookup"><span data-stu-id="1783d-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="1783d-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1783d-112">Required.</span></span> <span data-ttu-id="1783d-113">Eine Zeichenfolge, die den Text der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="1783d-113">String that contains the text of the query.</span></span> <span data-ttu-id="1783d-114">Dieser Parameter darf nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="1783d-114">This parameter cannot be blank.</span></span> <span data-ttu-id="1783d-115">Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="1783d-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-116">"in der *Sprache* \[ " optionale\]</span><span class="sxs-lookup"><span data-stu-id="1783d-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1783d-117">Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält.</span><span class="sxs-lookup"><span data-stu-id="1783d-117">String that contains the query language to be used.</span></span> <span data-ttu-id="1783d-118">Wenn angegeben, muss dieser Wert "WQL" lauten.</span><span class="sxs-lookup"><span data-stu-id="1783d-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="1783d-119">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1783d-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1783d-120">Eine ganze Zahl, die das Verhalten der Abfrage bestimmt und bestimmt, ob dieser Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1783d-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="1783d-121">Der Standardwert für diesen Parameter ist **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="1783d-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="1783d-122">Dieser Parameter kann die folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="1783d-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="1783d-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1783d-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-124">Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1783d-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="1783d-125">Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.</span><span class="sxs-lookup"><span data-stu-id="1783d-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="1783d-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemflagbidirektionale \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1783d-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-127">Bewirkt, dass WMI Zeiger auf Objekte der-Enumeration behält, bis der Client den Enumerator freigibt.</span><span class="sxs-lookup"><span data-stu-id="1783d-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="1783d-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1783d-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-129">Bewirkt, dass der-Rückruf sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1783d-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="1783d-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemflagreturn-Complete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1783d-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-131">Bewirkt, dass dieser-Vorgang blockiert wird, bis die Abfrage beendet ist.</span><span class="sxs-lookup"><span data-stu-id="1783d-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="1783d-132">Mit diesem Flag wird die-Methode im synchronen Modus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1783d-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="1783d-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemqueryflagprototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="1783d-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-134">Wird zum Prototypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1783d-134">Used for prototyping.</span></span> <span data-ttu-id="1783d-135">Dieses Flag verhindert, dass die Abfrage ausgeführt wird, und gibt ein Objekt zurück, das wie ein typisches Ergebnis Objekt aussieht.</span><span class="sxs-lookup"><span data-stu-id="1783d-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1783d-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1783d-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1783d-137">Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1783d-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="1783d-138">Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1783d-139">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1783d-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1783d-140">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1783d-140">Typically, this is undefined.</span></span> <span data-ttu-id="1783d-141">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1783d-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="1783d-142">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="1783d-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1783d-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1783d-143">Return value</span></span>

<span data-ttu-id="1783d-144">Wenn kein Fehler auftritt, gibt diese Methode ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1783d-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="1783d-145">Dies ist eine Objekt Auflistung, die das Resultset der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="1783d-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="1783d-146">Der Aufrufer kann die Auflistung mithilfe der Implementierung von Auflistungen für die verwendete Programmiersprache untersuchen.</span><span class="sxs-lookup"><span data-stu-id="1783d-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="1783d-147">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="1783d-148">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1783d-148">Error codes</span></span>

<span data-ttu-id="1783d-149">Nach dem Abschluss der **ExecQuery** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="1783d-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="1783d-150">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1783d-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-151">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="1783d-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-152">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1783d-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-153">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1783d-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1783d-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-155">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="1783d-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-156">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="1783d-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-157">Die Abfrage Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1783d-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="1783d-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-159">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1783d-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1783d-160">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1783d-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1783d-161">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1783d-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1783d-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1783d-162">Remarks</span></span>

<span data-ttu-id="1783d-163">**ExecQuery** ist einer der am häufigsten verwendeten Aufrufe zum Abrufen von WMI-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1783d-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="1783d-164">Ein standardmäßiger Befehl von **ExecQuery** sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="1783d-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="1783d-165">Beachten Sie, dass Sie das Objekt " [**bulbemservices**](swbemservices.md) " mit einem Moniker erstellen, der den entsprechenden Namespace und die Sicherheit darstellt, und dann den **ExecQuery** -Aufruf über den Dienst durchführen.</span><span class="sxs-lookup"><span data-stu-id="1783d-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="1783d-166">Eine ausführlichere Erläuterung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md) und [Aufzählen von WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="1783d-167">Wie die [**InstancesOf**](swbemservices-instancesof.md) -Methode gibt die **ExecQuery** -Methode immer eine [**errbewbjectset**](swbemobjectset.md) -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="1783d-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="1783d-168">Daher muss das WMI-Skript die Auflistung von ExecQuery-Rückgaben auflisten, um auf jede verwaltete Ressourcen Instanz in der Auflistung zuzugreifen, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="1783d-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="1783d-169">Andere " [**errbemservices**](swbemservices.md) "-Methoden, die ein " [**errbewbjectset**](swbemobjectset.md) " zurückgeben, umfassen [**associatorsof**](swbemservices-associatorsof.md), [**referencesto**](swbemservices-referencesto.md)und [**SubclassesOf**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="1783d-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="1783d-170">Es ist kein Fehler, wenn die Abfrage ein leeres Resultset zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1783d-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="1783d-171">Die **ExecQuery** -Methode gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die Key-Eigenschaft im " *strinquery* "-Argument angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="1783d-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="1783d-172">Wenn beim Ausführen dieser Methode ein Fehler auftritt und Sie das **wbemFlagReturnImmediately** -Flag nicht verwenden, wird das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt erst festgelegt, wenn Sie versuchen, auf den zurückgegebenen Objekt Satz zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1783d-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="1783d-173">Wenn Sie jedoch das **wbemflagreturnjecomplete** -Flag verwenden, wird das Err-Objekt festgelegt, wenn die **ExecQuery** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1783d-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="1783d-174">Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1783d-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="1783d-175">Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den Fehlercode für die **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1783d-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="1783d-176">Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="1783d-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="1783d-177">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1783d-177">Examples</span></span>

<span data-ttu-id="1783d-178">Im folgenden VBScript-Codebeispiel werden alle Laufwerke auf dem lokalen Computer und die Geräte-ID und der Typ des Laufwerks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1783d-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="1783d-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1783d-179">Requirements</span></span>



| <span data-ttu-id="1783d-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1783d-180">Requirement</span></span> | <span data-ttu-id="1783d-181">Wert</span><span class="sxs-lookup"><span data-stu-id="1783d-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1783d-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1783d-182">Minimum supported client</span></span><br/> | <span data-ttu-id="1783d-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1783d-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1783d-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1783d-184">Minimum supported server</span></span><br/> | <span data-ttu-id="1783d-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1783d-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1783d-186">Header</span><span class="sxs-lookup"><span data-stu-id="1783d-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="1783d-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1783d-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1783d-188">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1783d-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="1783d-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1783d-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1783d-190">DLL</span><span class="sxs-lookup"><span data-stu-id="1783d-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1783d-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1783d-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1783d-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="1783d-192">CLSID</span></span><br/>                    | <span data-ttu-id="1783d-193">CLSID- \_ Austauschdienste</span><span class="sxs-lookup"><span data-stu-id="1783d-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="1783d-194">IID</span><span class="sxs-lookup"><span data-stu-id="1783d-194">IID</span></span><br/>                      | <span data-ttu-id="1783d-195">IID \_ iswbemservices</span><span class="sxs-lookup"><span data-stu-id="1783d-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1783d-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1783d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1783d-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="1783d-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="1783d-198">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="1783d-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="1783d-199">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="1783d-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="1783d-200">Erstellen eines WMI-Skripts</span><span class="sxs-lookup"><span data-stu-id="1783d-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="1783d-201">Auflisten von WMI</span><span class="sxs-lookup"><span data-stu-id="1783d-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

